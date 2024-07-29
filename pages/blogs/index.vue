<template>
    <div class="w-full">
        <A-Nav></A-Nav>
        <div class="px-10 2xl:px-20 py-10 lg:py-10 xl:py-12 2xl:py-14 min-h-screen">
            <h1 class="text-5xl font-semibold">Blogs & Media</h1>

            <div v-if="isLoaded"
                class="flex flex-wrap justify-evenly xl:grid xl:grid-cols-3 2xl:grid-cols-4 mt-20 gap-x-10 gap-y-10">
                <NuxtLink v-for="item in sortedCollectionArray" :to="`/blogs/blog/${item.url}`"
                    class="w-full sm:w-80 transition-all block mr-auto duration-700 hover:opacity-75 active:opacity-80 cursor-pointer">
                    <div class="h-96 w-full">
                        <img :src="item.image" class="object-cover h-full rounded-lg w-full" alt="" />
                    </div>
                    <h3 class="w-full mt-4 font-semibold text-lg">
                        {{ item.title }}
                    </h3>
                </NuxtLink>
            </div>

            <div v-else class="w-full">
                <div class="min-h-screen w-full grid place-content-center">
                    <img src="@/assets/images/logo.svg" class="h-7 animate-pulse duration-500" alt="" />
                </div>
            </div>
        </div>
        <AFooter></AFooter>
    </div>
</template>

<script setup>

const collectionArray = ref([]);
const isLoaded = ref(false);
const client = useSupabaseClient();

onMounted(async () => {

    try {
        const { data, error } = await client
            .from("Invac Blogs")
            .select()
            .order("id", { ascending: true });
        if (error) throw error;
        collectionArray.value = data;
        console.log("collectionArray", collectionArray.value);
    } catch (error) {
        // Handle error
        console.log("error", error);
    }

    // Sort the collectionArray by title in alphabetical order
    collectionArray.value.sort((a, b) => a.title.localeCompare(b.title));
    isLoaded.value = true;
});

const sortedCollectionArray = computed(() => {
    console.log(
        "sortedCollectionArray computed property called",
        collectionArray.value
    );
    return collectionArray.value.sort((a, b) => a.title.localeCompare(b.title));
});
</script>
