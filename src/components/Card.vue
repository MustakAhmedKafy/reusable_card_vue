<script setup>
import Rating from "./Rating.vue";
const props = defineProps([
  "image",
  "location",
  "price",
  "rating",
  "title",
  "time",
]);
</script>

<template>
  <div>
    <div class="max-w-sm rounded overflow-hidden shadow-lg">
      <img class="w-full" :src="image" alt="" />
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">{{ title }}</div>
        <p class="text-gray-700 text-base">{{ location }}</p>
        <p class="text-gray-700 text-base">${{ price }}</p>
        <p class="text-gray-700 text-base">{{ time }} Days tour</p>
        <Rating :rating="rating" />
      </div>
    </div>
  </div>
</template>
