<script setup>
import MasonryCard from "./components/MasonryCard.vue";
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <div class="container__main">
    <div class="masonry-wrapper">
      <HelloWorld  />
      <div class="masonry-columns">
        <!-- <masonry-card v-for="($index, card) in 10" :key="$index"></masonry-card> -->
      </div>
    </div>
  </div>
</template>


