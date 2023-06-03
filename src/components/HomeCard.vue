<script setup>
import { toRefs } from "vue";
import { RouterLink } from "vue-router";

const props = defineProps({
  image: String,
});
const { image, title, subTitle } = toRefs(props);
</script>

<template>
  <RouterLink to="library">
    <img class="absolute z-0 w-[596px] right-0 top-0" :src="image" alt="" />
  </RouterLink>
</template>
