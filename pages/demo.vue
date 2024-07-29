<template>
    <div class="w-full relative">
        <div class="w-full lg:h-screen lg:flex">
            <div class="lg:w-[50%] lg:min-w-[50%] lg:h-full px-10 pb-20 lg:pb-0 lg:px-20 pt-20 text-white">
                <NuxtLink to="/">
                    <img src="@/assets/images/logo.svg" class="h-7" alt="" />
                </NuxtLink>

                <p class="tracking-[0.6rem] text-xl mt-20 lg:mt-44">Contact Us</p>

                <h2 class="lg:mt-44 text-4xl mt-20 lg:text-6xl font-semibold">
                    <span class="text-[#FF7900]">Product</span>
                    <span class="block font-medium mt-3">Enquiry / Demo</span>
                </h2>
            </div>
            <div class="lg:w-[50%] bg-white text-black lg:min-w-[50%] h-full pt-14 pb-10 px-10 lg:px-20 grid">
                <div class="w-full flex justify-end items-center place-self-start min-h-fit max-h-fit">


                    <NuxtLink class="hidden lg:block" to="/">
                        <img src="@/assets/icons/x.svg" class="h-10 w-10" alt="" />
                    </NuxtLink>
                </div>

                <form @submit.prevent="submitForm" class="place-self-end w-full flex flex-col gap-y-14">
                    <!-- <input v-model="name" type="text"
                        class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                        placeholder="Name*" />
                    <input v-model="email" type="email"
                        class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                        placeholder="Email ID*" />
                    <input v-model="phone" type="text"
                        class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                        placeholder="Phone No*" />

                    <input v-model="city" type="text"
                        class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                        placeholder="City" />
                    -->
                    <div>
                        <input v-model="nameRef" type="text" required
                            class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                            placeholder="Name*" :class="{ 'border-red-500': !isNameValid }" />
                        <!-- Display error message if name is not valid -->
                        <span v-if="!isNameValid" class="text-red-500">Name should not contain special characters or
                            numbers.</span>
                    </div>
                    <div>
                        <input v-model="emailRef" type="email" required
                            class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                            placeholder="Email ID*" :class="{ 'border-red-500': !isEmailValid }" />
                        <!-- Display error message if email is not valid -->
                        <span v-if="!isEmailValid" class="text-red-500">Please enter a valid email address.</span>
                    </div>
                    <div>
                        <input v-model="phoneRef" type="text" required
                            class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                            placeholder="Phone No*" :class="{ 'border-red-500': !isPhoneValid }" />
                        <!-- Display error message if phone number is not valid -->
                        <span v-if="!isPhoneValid" class="text-red-500">Phone number should be 10 digits long.</span>

                    </div>
                    <div>
                        <input v-model="cityRef" type="text" required
                            class="w-full outline-none text-lg lg:text-2xl border-neutral-600 border-b-2 pb-3"
                            placeholder="City*" :class="{ 'border-red-500': !isCityValid }" />
                        <!-- Display error message if city is not valid -->
                        <span v-if="!isCityValid" class="text-red-500">Please enter a valid city name.</span>

                    </div>
                    <div class="lg:w-full pb-3 flex text-lg lg:text-2xl justify-between border-b-2 border-black">
                        <select v-model="typeOfHome" class="w-full outline-none">
                            <option value="apartment">Apartment</option>
                            <option value="independent-house">Independent Home</option>
                        </select>
                        <label for="model">
                            <img src="@/assets/icons/chevron-down.svg" class="h-10 w-10" alt="" />
                        </label>
                    </div>

                    <div class="lg:flex justify-between">
                        <div class="lg:w-[45%] pb-3 flex text-lg lg:text-2xl justify-between border-b-2 border-black">
                            <select v-model="sizeOfHome" class="w-full outline-none">
                                <option value="2000-sft">&lt; 2000 Sft Built Up Area</option>
                                <option value="2000-3000-sft">2000 - 3000 Sft Built Up Area</option>
                                <option value="3000-5000-sft">3000 - 5000 Sft Built Up Area</option>
                                <option value="5000-10000-sft">5000 - 10000 Sft Built Up Area</option>
                                <option value="10000-sft">&gt; 10000 Sft Built Up Area</option>
                            </select>
                            <label for="model">
                                <img src="@/assets/icons/chevron-down.svg" class="h-10 w-10" alt="" />
                            </label>
                        </div>

                        <div
                            class="lg:w-[45%] mt-12 lg:mt-0 pb-3 flex text-lg lg:text-2xl justify-between border-b-2 border-black">
                            <select v-model="currentStage" class="w-full outline-none">
                                <option value="under-construction">Under Construction</option>
                                <option value="interior-under-construction">Interior Under Construction</option>
                                <option value="fully-constructed">Fully Constructed</option>
                            </select>
                            <label for="model">
                                <img src="@/assets/icons/chevron-down.svg" class="h-10 w-10" alt="" />
                            </label>
                        </div>
                    </div>

                    <button type="submit" class="flex ml-auto w-fit my-2 lg:my-14">
                        <span class="text-4xl tracking-[0.6rem] opacity-70 cursor-pointer">Send</span>
                        <img src="@/assets/icons/orange-arrow-right.svg" class="h-10 ml-3" alt="" />
                    </button>
                </form>
            </div>
        </div>

        <div v-if="submittedState"
            class="h-screen w-full font-semibold flex flex-col gap-y-6 justify-center items-center text-center fixed top-0 z-50 px-10 bg-white">
            <h3>
                <img src="@/assets/icons/logo-white.svg" class="h-7 lg:h-7 xl:h-8 2xl:h-9 animate-bounce duration-500"
                    alt="">
            </h3>
            <h3 class=" text-lg lg:text-xl text-black">Thank you</h3>
            <h3 class=" text-lg lg:text-xl text-black">
                Thank you, we will get back to you shortly.
            </h3>
        </div>
    </div>
</template>
  
<script setup>
useHead({
    title: `Experience InVac Central Vacuum System | Schedule Your Demo Now`,
    meta: [
        {
            name: 'description',
            content: `Explore the potential of our products by booking a demo now for an engaging interaction.`
        }
    ]
})


definePageMeta({
    scrollToTop: true,
    pageTransition: false,
});
const nameRef = ref("");
const emailRef = ref("");
const phoneRef = ref("");
const cityRef = ref("");
const typeOfHome = ref("apartment");
const sizeOfHome = ref("2000-sft");
const currentStage = ref("under-construction");
const router = useRouter()
const submittedState = ref(false)
const date = new Date()
const WEB3FORMS_ACCESS_KEY = "298883d0-8170-41ea-8f34-2663da8986c0";

const isNameValid = computed(() => nameRef.value ? /^[A-Za-z\s]+$/.test(nameRef.value) : true);
const isEmailValid = computed(() => emailRef.value ? /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(emailRef.value) : true);
const isPhoneValid = computed(() => phoneRef.value ? /^\d{10}$/.test(phoneRef.value) : true);
const isCityValid = computed(() => cityRef.value ? /^[A-Za-z\s]+$/.test(cityRef.value) : true);

const submitForm = async () => {
    const formData = {
        access_key: WEB3FORMS_ACCESS_KEY,
        name: nameRef.value,
        email: emailRef.value,
        phone: phoneRef.value,
        city: cityRef.value,
        typeOfHome: typeOfHome.value,
        sizeOfHome: sizeOfHome.value,
        currentStage: currentStage.value,
        currentDate: date
    };
    if (isNameValid._value && isEmailValid._value && isPhoneValid._value && isCityValid._value) {

        try {

            const response = await fetch("https://api.web3forms.com/submit", {
                method: "POST",
                headers: {
                    "Content-Type": "application/json",
                    Accept: "application/json",
                },
                body: JSON.stringify(formData),
            });
            const result = await response.json();
            if (result.success) {
                console.log(result);
            }
            submittedState.value = true
            submittedState.value = false
            router.push('/thank-you')

        }



        catch (error) {
            console.log(error.message)
        }
    }

};
</script>
  
<style scoped>
select {
    appearance: none;
}
</style>
  
