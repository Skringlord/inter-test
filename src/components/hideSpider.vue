<template>
  <div class="spider-task-container">
    <button v-on:click="hideSpider = !hideSpider">toggle spider</button>
    <transition name="hideSpider" v-if="hideSpider">
      <div class="spider">///(0_0)\\\</div>
    </transition>
    <p v-else>
      {{ "spider is hidden" }}
    </p>
  </div>
</template>

<script>
export default {
  name: "HideSpider",
  data() {
    return {
      hideSpider: false,
    };
  },
};
</script>

<style scoped>
.spider-task-container {
  display: flex;
  padding-top: 150px;
  width: 100%;
  height: 500px;
  flex-direction: column;
  align-items: center;
}

p {
  text-align: center;
}

button {
  height: 90px;
  width: max-content;
  font-size: 50px;
  margin: 25px;
}

.spider {
  font-size: 72px;
  color: orangered;
}

.hideSpider-enter-active {
  animation: moveEnter 1s;
}

.hideSpider-leave-active {
  animation: moveLeave 1s;
}

@keyframes moveEnter {
  100% {
    opacity: 1;
    scale: 1;
  }
  0% {
    opacity: 0;
    scale: 0;
  }
}

@keyframes moveLeave {
  0% {
    opacity: 1;
    scale: 1;
  }
  100% {
    opacity: 0;
    scale: 0;
  }
}
</style>