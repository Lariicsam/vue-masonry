<script>
export default {
  methods: {
    showOverlay() {
      this.$emit("showOverlay");
    },
  },
};
</script>
<template>
  <div
    class="masonry-item"
    style="
      background-image: url('https://nacms-production.s3.amazonaws.com/50264/out..jpeg');
    "
    @mouseenter="showOverlay"
  >
    <div class="masonry-overlay">
      <i class="masonry-fav-alone"></i>
      <i class="masonry-edit"></i>
      Alexcoal, Drawn By Alberto Vargas, Glamourous, Elegant, Sophisticated
    </div>
    <span class="masonry-counter hide"
      >6840<i class="masonry-fav-filled"></i
    ></span>
  </div>
</template>