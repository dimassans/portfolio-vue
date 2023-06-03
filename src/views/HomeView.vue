<script setup>
import HomeCard from "@/components/HomeCard.vue";
</script>

<template>
  <div class="p-8">
    <div class="flex items-center">
      <HomeCard image="../public/images/image/Profile.png" title="Title is here" subTitle="Subtitle is here" />
    </div>
    <div class="py-[140px] px-[8px]">
      <h1 class="text-white text-2xl font-bold">DIMAS TRI SAPUTRA</h1>
      <div class="py-1"></div>
      <h6 class="text-white text-base font-semibold">Front-end Development</h6>
      <div class="py-2"></div>
      <p class="text-white text-base w-[608px] z-5">
        Mendalami bidang Desainer UI/UX dan pemrograman web dasar. Saya tertarik dengan web front-end pengembangan dan ilustrasi. Saya memiliki pengalaman membuat desain ilustrasi untuk desain kebutuhan dan membuat desain UI/UX di aplikasi
        Figma.
      </p>
      <div class="py-3"></div>
      <RouterLink to="contact">
        <button to="Contact" type="button" class="bg-red-600 hover:bg-red-900 text-white font-semibold py-2 px-4 rounded-lg">Hire Me</button>
      </RouterLink>
      <div class="py-1"></div>
    </div>
  </div>
</template>
