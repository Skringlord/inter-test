<template>
  <div id="app">
    <BaseButton>I'm a button</BaseButton>
    {{ changeMe }}
    <MoveArrow></MoveArrow>
  </div>
</template>

<script>
import BaseButton from "./components/UI/BaseButton.vue";
import MoveArrow from "./components/hideSpider.vue";

export default {
  name: "App",
  data() {
    return {
      changeMe: {
        imNull: null,
      },
    };
  },
  components: { BaseButton, MoveArrow },
  methods: {
    buttonMethod(data) {
      console.log(data);
    },
  },
  mounted() {
    const itemsMockData = [1, 2, 3, 4, 5, 6, 6, 7, 78, 8, 9, 1];

    setTimeout(() => (this.changeMe.itemsData = itemsMockData), 2000);

    setTimeout(() => (this.changeMe.itemsData[5] = "A"), 2500);

    setTimeout(() => (this.changeMe.itemsData[5] = "B"), 3500);

    // don't touch console.log
    // please
    setTimeout(() => console.log(this.changeMe.itemsData), 5000);
  },
};
</script>

<style>
#app {
  margin: 0;
  font-size: 32px;
}
</style>
