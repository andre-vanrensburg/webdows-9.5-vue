<script>
// this will include all imports of components
import TaskBar from "./components/TaskBar.vue";
import Window from "./components/Window.vue";
import Icons from "./components/Icons.vue";

export default {
  name: "app",
  components: {
    TaskBar,
    Window,
    Icons,
  },
};
</script>

<template>
  <!--this will include components like icons, modal window, taskbar etc.-->
  <Window />
  <Icons />
  <TaskBar />
</template>

<style scoped></style>
