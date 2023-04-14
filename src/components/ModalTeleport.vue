<template>
  <div class="modals">
    <h1>Modals</h1>
    <button>show modal</button>

    <div v-if="showModal" class="modal">
      <h3>This is a modal</h3>
      <button>Hide modal</button>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";

const showModal = ref(false)
</script>

<style>
  .modal {
    background-color: rgba(0, 0, 0, 0.8);
    padding: 8px;
    color: beige;
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0;
    top: 0;
    z-index: 8;
  }
</style>