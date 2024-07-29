<template>
    <div class="w-full">
        <NuxtPage></NuxtPage>
    </div>
</template>

<script setup>
useHead({
    title: `Improve Your Cleaning Appliances | Central Vacuum System Accessories | InVac`,
    meta: [
        {
            name: 'description',
            content: `For efficient cleanup, enhance your central vacuum system with premium accessories. Check a range of products and attachments for the best performance and comfort of handling.`
        }
    ]
})

useSeoMeta({
    title: `Improve Your Cleaning Appliances | Central Vacuum System Accessories | InVac`,
})

const forHomeState = ref(false)

definePageMeta({
    scrollToTop: true,
    pageTransition: false,
});
</script>

<style lang="scss" scoped></style>
