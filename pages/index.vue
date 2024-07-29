<template>
  <div :style="{ opacity: opacity }" class="w-full bg-[#1A1A1A]">
    <H-Header />
    <H-Second />
    <H-Third />
    <H-Fourth />
    <H-Five></H-Five>
    <H-Sixth />
    <H-Seventh></H-Seventh>
    <H-Eight></H-Eight>
    <A-Footer />
  </div>
</template>


<script setup>
  useHead({
    title: `Wet And Dry Central Vacuum System | Central Vacuum Cleaner | InVac`,
    meta: [
        {
            name: 'description',
            content: `Reach the next level of cleaning with InVac central vacuum system. It's a modern solution to a spotlessly clean home quiet, strong, and simple to operate.`
        }
    ]
})

definePageMeta({
  scrollToTop: true,
  pageTransition: false,
});



</script>
<script>
export default {
  data() {
    return {
      opacity: 1, 
    };
  },
  mounted() {
    
  }
};
</script>