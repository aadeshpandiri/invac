<template>
    <div
      @click.self="citiesState = false"
      class="fixed top-0 h-screen w-full grid place-content-center cursor-pointer bg-black bg-opacity-30"
    >
      <div class="w-[95vw] h-fit cursor-default bg-white text-black rounded-xl p-5 lg:p-10">
        <div class="flex justify-between items-center">
          <div class="flex gap-x-4 lg:gap-x-3 items-center">
            <p class="text-base lg:text-4xl">Cities We Are At</p>
            <img src="../assets/icons/orange-arrow-right.svg" class="h-5 lg:h-8 lg:ml-10" alt="" />
          </div>
  
          <img src="@/assets/icons/logo-white.svg" class="h-5 lg:h-7" alt="" />
        </div>
  
        <div
          class="h-full mt-10 grid grid-cols-3 lg:grid-cols-5 xl:grid-cols-6 2xl:grid-cols-8 justify-between gap-y-7 text-xs sm:text-sm pb-10 lg:mt-20 lg:text-base"
        >
          <p>Chennai</p>
          <p>Manglore</p>
          <p>Callcut</p>
          <p>Surat</p>
          <p>Jaipur</p>
          <p>Kolkata</p>
          <p>Vijayawds</p>
          <p>Coimbatore</p>
          <p>Banglore</p>
          <p>Mumbai</p>
          <p>Ahmedabad</p>
          <p>Raipur</p>
          <p>Chandigarh</p>
          <p>Vishakapatnam</p>
          <p>Tirpur</p>
          <p>Kochi</p>
          <p>Pune</p>
          <p>New Delhi</p>
          <p>Indore</p>
          <p>Ludhiana</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const citiesState = useState("citiesState");
  </script>