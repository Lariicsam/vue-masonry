<template>
  <div class="icol center">
    <div class="irow center">
      <h1>{{ myNonReactiveData }}</h1>
    </div>
    <div class="irow center">
      <h2>{{ counterData.title }}:</h2>
      <div class="btn" @click="decreaseCounter(2)">--</div>
      <div class="btn" @click="decreaseCounter(1)">-</div>
      <strong class="counter">{{ counterData.count }}</strong>
      <div class="btn" @click="increaseCounter(1)">+</div>
      <div class="btn" @click="increaseCounter(2)">++</div>
    </div>

    <div class="irow center">
      <p>This counter is {{ oddOrEven }}</p>
    </div>
    <div class="irow center">
      <div class="icol md">
        <h4 class="edit">Edit counter title:</h4>
        <input v-model="counterData.title" type="text" class="edit-input" />
      </div>
    </div>
  </div>
</template>

<script>
import { reactive, computed } from "vue";
export default {
  setup() {
    const myNonReactiveData = "My static Non reactive Title";

    const oddOrEven = computed(() => {
      if (counterData.count % 2 === 0) {
        return "even";
      } else {
        return "odd";
      }
    });

    const increaseCounter = (amount) => {
      counterData.count += amount;
    };
    const counterData = reactive({ count: 0, title: "My Title" });
    const decreaseCounter = (amount) => {
      counterData.count -= amount;
    };

    return {
      myNonReactiveData,
      increaseCounter,
      decreaseCounter,
      counterData,
      oddOrEven
    };
  },
};
</script>


<style>
  .btn,
  .counter {
    font-size: 40px;
    padding: 20px;
    width: 100px;
    cursor: pointer;
  }

  .edit {
    font-size: 32px;
    text-align: center;
  }

  .edit-input {
    border: 1px solid azure;
    background-color: white;
    border-radius: 16px;
    padding: 8px 0;
    font-weight: lighter;
    font-size: 24px;
    color: green;
    text-align: center;
  }
</style>
 
