<script setup>
import MasonryCard from "./components/MasonryCard.vue";
</script>

<template>
  <div class="container__main">
    <div class="masonry-wrapper">
      <div class="masonry-columns">
        <masonry-card v-for="($index, card) in 10" :key="$index"></masonry-card>
      </div>
    </div>
  </div>
</template>

