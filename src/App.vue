<script setup>
import Card from "./components/Card.vue";

const data = [
  {
    image: "img/product-1.jpg",
    location: "California",
    price: 87,
    rating: 3,
    time: 15,
    title: "Photo by drew",
  },
  {
    image: "img/product-2.jpg",
    location: "Los Angels",
    price: 90,
    rating: 5,
    time: 17,
    title: "Photo by Mustak",
  },
];
</script>

<template>
  <div>
    <!-- <Card
      v-for="item in data"
      :key="item.title"
      :image="item.image"
      :location="item.location"
      :price="item.price"
      :rating="item.rating"
      :time="item.time"
      :title="item.title"
    /> -->
    <div class="container mx-auto">
      <div class="md:flex md:flex-wrap">
        <div class="md:w-1/2 px-4 mb-8">
          <Card v-for="item in data" :key="item.title" v-bind="item" />
        </div>
      </div>
    </div>
  </div>
</template>
