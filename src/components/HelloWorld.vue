<template>
  <div class="icol center">
    <div class="irow center">
      <h1>{{ myNonReactiveData }}</h1>
    </div>
    <div class="irow center">
      <h2>{{ counterData.title }}:</h2>
      <div class="btn" @click="decreaseCounter">-</div>
      <strong class="counter">{{ counterData.count }}</strong>
      <div class="btn" @click="increaseCounter">+</div>
    </div>
    <div class="irow center">
      <div class="edit">
        <h4>Edit counter title:</h4>
        <input v-model="counterData.title" type="text" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  setup() {
    const myNonReactiveData = "My static Non reactive Title"
    const counter = ref(0),
      counterTitle = ref("My Counter");

    const increaseCounter = () => {
      //counter.value++;
      counterData.count++;
    };

    const counterData = reactive({ count: 0, title: "My Title" });

    const decreaseCounter = () => {
      //counter.value--;
      counterData.count--;
    };

    return {
      myNonReactiveData,
      counter,
      counterTitle,
      increaseCounter,
      decreaseCounter,
      counterData,
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

  .edit,
  .edit > input {
    color: darkgreen;
  }
</style>
 
