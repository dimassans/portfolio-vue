<script setup>
import ProjectCard from "../components/ProjectCard.vue";
</script>

<template>
  <div class="p-8">
    <h1 class="text-white text-3xl font-bold">Yukk, belajar web programming bersama</h1>
    <div class="py-2"></div>
    <p class="text-white text-base w-[608px] z-5">Beberapa project dan tugas pembelajaran yang saya kerjakan selama kuliah</p>
    <div class="py-2"></div>
    <h1 class="text-white text-lg font-semibold">My Project</h1>

    <div class="py-1.5"></div>

    <div class="flex items-center">
      <a href="https://drive.google.com/drive/u/0/folders/1jYcW_rxqHpFJv72zZEsJQINl_bmRlw_X"> <ProjectCard image="../public/images/image/Project1.png" title="Login Page" subTitle="2021" /></a>
      <ProjectCard image="../public/images/image/Project2.png" title="UI/UX Design" subTitle="2022" />
      <ProjectCard image="../public/images/image/Project3.jpeg" title="Web Portfolio" subTitle="2023" />
    </div>
  </div>
</template>
