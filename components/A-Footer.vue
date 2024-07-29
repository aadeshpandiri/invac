<template>
    <div class="w-full px-10 lg:px-20 pt-20 pb-20">
        <h2 class="text-5xl lg:text-7xl">
            <div class="overflow-y-clip">
                <span class="block translate-y-[100%] footer-anim-pop-wide">Let's</span>
            </div>

            <div class="overflow-y-clip">
                <span class="block mt-3 font-bold translate-y-[100%] footer-anim-pop-wide">Get in touch</span>
            </div>

        </h2>

        <div class="lg:flex items-center justify-between mt-10">
            <div class="flex gap-x-16 items-center lg:w-[50%]">
                <a class="overflow-y-clip block" href="https://www.facebook.com/Invacindia">
                    <img src="@/assets/icons/facebook.svg" class="h-8 block translate-y-[100%] footer-anim-pop-wide" alt="">
                </a>
                <a class="overflow-y-clip block" href="https://instagram.com/invac_india">
                    <img src="@/assets/icons/instagram.svg" class="h-8 block translate-y-[100%] footer-anim-pop-wide"
                        alt="">
                </a>
                <a class="overflow-y-clip block" href="https://twitter.com/IndiaInvac">
                    <img src="@/assets/icons/twitter.svg" class="h-8 block translate-y-[100%] footer-anim-pop-wide" alt="">
                </a>
                <a class="overflow-y-clip block" href="https://www.linkedin.com/company/invac-india/">
                    <img src="@/assets/icons/linkdin.svg" class="h-8 block translate-y-[100%] footer-anim-pop-wide" alt="">
                </a>
            </div>

            <a href="tel:+919248009941"
                class="items-center mt-20 lg:mt-0 grid-flow-col gap-x-5 lg:w-[50%] flex lg:grid lg:place-content-center lg:pl-[15%]">
                
                <div class="overflow-y-clip">
                    <img class="footer-anim-pop-wide"
                        src="@/assets/images/home-static/telephone-handle-silhouette.png" alt="">
                </div>
                <div class="overflow-y-clip">
                    <p class="text-lg translate-y-[100%] footer-anim-pop-wide">Call Us</p>
                </div>
            </a>

            <div class="w-full bg-neutral-500 rounded-sm h-1 mt-10 lg:hidden"></div>
        </div>


        <div class="mt-10 lg:mt-20">
            <div class="flex items-center overflow-y-clip">
                <img src="@/assets/images/logo.svg" class="h-7 translate-y-[140%] footer-anim-pop-wide" alt="">
                <div class="flex flex-col text-sm ml-4 min-w-fit translate-y-[100%] footer-anim-pop-wide">
                    <p class="">Central</p>
                    <p class="text-[#f16012]">Vacuum System</p>
                </div>

                <div class="h-1 w-0 line-expand-footer bg-white ml-40 rounded-sm hidden lg:block"></div>
            </div>
        </div>

        <div class="w-full lg:grid lg:grid-cols-2 mt-20">
            <div>
                <div class="text-2xl font-semibold footer-anim-pop-wide">
                    <div class="translate-y-[100%] footer-anim-pop-wide"></div>
                </div>
                <div class="text-lg mt-10">
                    <div class="overflow-y-clip">
                        <div class="translate-y-[100%] footer-anim-pop-wide"> Invac India,</div>
                    </div>


                    <div class="overflow-y-clip">
                        <div class="translate-y-[100%] footer-anim-pop-wide"> 4th floor,Fortune Monarch Towers,</div>
                    </div>


                    <div class="overflow-y-clip">
                        <div class="translate-y-[100%] footer-anim-pop-wide"> Road No.36, Jubilee Hills,</div>
                    </div>


                </div>

                <a href="https://goo.gl/maps/fYzr3qNC6o45GugKA" class="text-lg mt-5 block overflow-y-clip">
                    <div class="footer-anim-pop-wide translate-y-[100%] flex gap-x-14">
                        <span>Hyderabad - 500033</span> <img src="@/assets/icons/orange-arrow-right.svg" class="h-6" alt="">
                    </div>
                </a>

                <div class="w-full hidden lg:flex gap-x-24 text-xl mt-24 overflow-y-clip">
                    <a class="footer-anim-pop-wide translate-y-[100%]" href="mailto:sales@invac.in">sales@invac.in</a>
                    <a class="footer-anim-pop-wide translate-y-[100%]" href="tel:+91 8798 779 778">+91 9248009941</a>
                </div>


            </div>

            <div class="w-full h-0.5 bg-neutral-400 mt-10 lg:hidden"></div>

            <div class="lg:pl-[20%] mt-10 lg:mt-0 lg:h-full lg:flex lg:flex-col lg:flex-grow lg:justify-between">
                <!-- <div class="text-2xl font-semibold overflow-y-clip">
                    <div class="footer-anim-pop-wide translate-y-[100%]">
                        Be Part of Invac Family
                    </div>
                </div>
                <p class="text-base mt-5 text-neutral-300">
                <div class="overflow-y-clip">
                    <div class="translate-y-[100%] footer-anim-pop-wide">
                        Keep up to Date with
                    </div>

                    <div class="translate-y-[100%] footer-anim-pop-wide">
                        exclusive projects
                    </div>

                </div>
                </p>
                <div>
                    <input type="text" placeholder="Your Name"
                        class="bg-transparent mt-12 text-xl lg:text-2xl border-b border-white pb-3 w-full outline-none">
                    <input type="text" placeholder="Email Address"
                        class="bg-transparent mt-10 text-xl lg:text-2xl border-b border-white pb-3 w-full outline-none">
                </div>


                <div class="text-lg font-semibold  overflow-y-clip flex gap-x-4 mt-8"> <span
                        class="border-b translate-y-[100%] footer-anim-pop-wide"> Subscribe</span> <img
                        class="translate-y-[100%] footer-anim-pop-wide" src="@/assets/icons/chevron-right.svg" alt="">
                </div> -->
                <div>
                    <h2 class="font-semibold text-xl mt-24 text-[#f16012]">Popular Searches</h2>
                    <div class="w-full text-sm lg:text-sm mt-10">
                        <div v-for="item in sortedCollectionArray" class="inline">
                            <NuxtLink :to="item.to"
                                class="hover:text-[#f16012] cursor-pointer transition-colors duration-700"> {{ item.title }}
                            </NuxtLink> |
                        </div>

                    </div>
                </div>
            </div>
        </div>

        <div class="mt-10 h-0.5 w-full bg-neutral-500 lg:hidden"></div>
        <div class="flex items-center justify-between mt-14 lg:mt-24">
            <div class="hidden overflow-y-clip lg:flex gap-x-20 text-neutral-400 text-sm">
                <span class="translate-y-[100%] footer-anim-pop-wide">© 2023 - Invac</span>

                <NuxtLink class="translate-y-[100%] footer-anim-pop-wide" to="/privacy-policy">Privacy Policy</NuxtLink>
            </div>

            <div class="flex text-xl flex-col lg:flex-row gap-y-14 lg:gap-y-0 overflow-y-clip lg:items-center lg:gap-x-20">
                <NuxtLink to="/terms-of-service"
                    class="flex items-center gap-x-4 translate-y-[100%] footer-anim-pop-wide text-neutral-400"> <span>Terms
                        of
                        service</span> <img src="@/assets/icons/orange-arrow-right.svg" class="h-6" alt=""> </NuxtLink>

                <NuxtLink to="/shipping-and-cancellation"
                    class="flex items-center gap-x-4 translate-y-[100%] footer-anim-pop-wide text-neutral-400">
                    <span>Shipping
                        & Cancellation</span> <img src="@/assets/icons/orange-arrow-right.svg" class="h-6" alt="">
                </NuxtLink>

                <div @click="citiesState = true"
                    class="flex items-center gap-x-4 text-neutral-400 translate-y-[100%] footer-anim-pop-wide cursor-pointer">
                    <span>Cities we are at</span> <img src="@/assets/icons/orange-arrow-right.svg" class="h-6" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script setup >
import gsap from 'gsap';

const sortedCollectionArray = ref([
    { to: '/accessories/floor-brush-without-wheels-horse-hair', title: 'floor brush cleaner' },
    { to: '/accessories/floor-brush-without-wheels-horse-hair', title: 'central vac floor brush' },
    { to: '/accessories/carpet-brush', title: 'Carpet Brush' },
    { to: '/accessories/carpet-brush', title: 'hard carpet brush' },
    { to: '/accessories/reversible-brush-without-wheels-horse-hair', title: 'Reversible Brush' },
    { to: '/accessories/dusting-tool', title: 'dusting brush' },
    { to: '/accessories/squeegee-on-wheels', title: 'squeegee' },
    { to: '/accessories/squeegee-on-wheels', title: 'floor squeegee' },
    { to: '/accessories/mop', title: 'Mop Without wheels Horse hair' },
    { to: '/accessories/mop', title: 'central vacuum mop' },
    { to: '/accessories/delicate-dust', title: 'Delicate Dust Brush' },
    { to: '/accessories/crevice-tool', title: 'Crevice Tool' },
    { to: '/accessories/crevice-tool', title: 'crevice cleaning brush' },
    { to: '/accessories/upholstery-tool', title: 'Upholstry Tool' },
    { to: '/accessories/upholstery-tool', title: 'upholstry brush' },
    { to: '/accessories/stainless-steel', title: 'Stainless steel Carpet Tools' },
    { to: '/accessories', title: 'Accessories for Central Vacuum' },
    { to: '/accessories/cabinet-vac', title: 'Kitchen Cabinet Central Vacuums' },
    { to: '/accessories/kick-vac', title: 'KickVac for Kitchen Cabinet' },
    { to: '/accessories/kick-vac', title: 'KickVac Kitchen' },
    { to: '/accessories/drawer-vac', title: 'Drawer Vac for Morden Kitchen' },
    { to: '/accessories/speedy-vac', title: 'Speedy Vac for Bathrooms' },
    { to: '/accessories/retra-vac', title: 'Retra Vac for Messy Cables' },
    { to: '/blogs/blog/Meta', title: 'Top Central Vacuum System' }
]);

//TODO change out collection images to white images no more blm
const citiesState = useState("citiesState");
onMounted(async () => {
    gsap.to('.footer-anim-pop-wide', {
        scrollTrigger: {
            trigger: ".footer-anim-pop-wide"
        },
        y: 0,
        duration: 0.7,
        stagger: 0.08
    })

    gsap.to('.line-expand-footer', {
        scrollTrigger: {
            trigger: ".footer-anim-pop-wide"
        },
        width: '100%',
        duration: 2.5,

    })




    // Sort the collectionArray by title in alphabetical order 
    //@ts-ignore

})
</script>
