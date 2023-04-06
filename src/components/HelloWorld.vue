<template>
  <div class="icol center">
    <div class="irow center">
      <div class="btn" @click="decreaseCounter">-</div>
      <strong class="counter">{{ counter }}</strong>
      <div class="btn" @click="increaseCounter">+</div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const counter = ref(0);

    const increaseCounter = () => {
      counter.value++;
    };
    const decreaseCounter = () => {
      counter.value--;
    };

    return {
      counter,
      increaseCounter,
      decreaseCounter
    };
  },
};
</script>



<!-- <script>
export default {
  data() {
    return {
      counter: 0,
    };
  },

  methods: {
    increaseCounter() {
      this.counter++;
    },

    decreaseCounter() {
      this.counter--;
    },
  },
};
</script> -->

<style>
  .btn,
  .counter {
    font-size: 40px;
    padding: 20px;
    width: 100px;
    cursor: pointer;
  }
</style>
 
