<script setup>
import { ref, onMounted } from "vue";
import { RouterLink, RouterView } from "vue-router";
import MenuItem from "./components/MenuItem.vue";

import HomeOutline from "vue-material-design-icons/HomeOutline.vue";
import TrendingUp from "vue-material-design-icons/Details.vue";
import Contacts from "vue-material-design-icons/Contacts.vue";
</script>

<template>
  <div>
    <div id="SideNav" class="flex z-40 items-center w-[120px] h-screen bg-black relative">
      <RouterLink to="/">
        <img class="absolute top-0 w-[46px] mt-10 ml-10" width="125" src="/images/icons/Logo.png" />
      </RouterLink>
      <div class="py-2 mx-2"></div>
      <ul>
        <RouterLink to="/">
          <MenuItem class="ml-[2px] mt-2" :iconSize="24" name="Home" iconString="home" pageUrl="/" />
        </RouterLink>
        <RouterLink to="/project">
          <MenuItem class="ml-[2px] mt-2" :iconSize="24" name="Project" iconString="library" pageUrl="/project" />
        </RouterLink>
        <RouterLink to="/contact">
          <MenuItem class="ml-[2px] mt-2" :iconSize="24" name="Contact" iconString="contact" pageUrl="/contact" />
        </RouterLink>
      </ul>
    </div>
  </div>
  <div class="fixed right-0 top-0 w-[calc(100%-120px)] overflow-auto h-full bg-black">
    <div class="mt-[18px]"></div>
    <RouterView />
    <div class="mb-[100px]"></div>
  </div>
</template>
