<script>
import TaskBar from "./components/TaskBar.vue";
import Window from "./components/Window.vue";
import Icons from "./components/Icons.vue";
// import Boot from "./components/Boot.vue";
// import Prompt from "./components/Prompt.vue";
// import Loading from "./components/Loading.vue";

export default {
  name: "app",
  components: {
    TaskBar,
    Window,
    Icons,
    // Boot,
    // Prompt,
    // Loading,
  },
};
</script>

<template>
  <Window />
  <Icons />
  <TaskBar />
  <!-- <Boot />
  <Prompt />
  <Loading /> -->
</template>

<style scoped></style>
