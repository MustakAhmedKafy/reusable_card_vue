<script setup>
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
        <div class="flex">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-star-fill"
            viewBox="0 0 16 16"
            v-for="index in rating"
            :key="index"
          >
            <path
              d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>
