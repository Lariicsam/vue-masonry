<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div
    class="masonry-item"
    style="
      background-image: url('https://nacms-production.s3.amazonaws.com/50264/out..jpeg');
    "
  >
    <div class="masonry-overlay">
      <i class="masonry-fav-alone"></i>
      <i class="masonry-edit"></i>
      <strong>{{ $i }}</strong>
      Alexcoal, Drawn By Alberto Vargas, Glamourous, Elegant, Sophisticated, Tar
      Vintage, Pin Up, Alluring, Seductive, [ tarot card ]!!!!!, black hair,
      full fac...
    </div>
    <span class="masonry-counter hide"
      >6840<i class="masonry-fav-filled"></i
    ></span>
  </div>
</template>