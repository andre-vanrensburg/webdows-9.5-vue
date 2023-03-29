<script>
import StartMenu from "./StartMenu.vue";

export default {
  name: "TaskBar",
  components: {
    name: StartMenu,
  },
  data() {
    return {
      hours: 0,
      minutes: 0,
    };
  },
  mounted() {
    setInterval(() => this.setTime(), 1000);
    // Time tooltip
    var timeTip = new Date().toLocaleDateString();
    document.getElementById("timetip").setAttribute("title", timeTip);
  },
  methods: {
    setTime() {
      const date = new Date();
      let hours = date.getHours();
      let minutes = date.getMinutes();
      hours = hours <= 9 ? `${hours}`.padStart(2, 0) : hours;
      minutes = minutes <= 9 ? `${minutes}`.padStart(2, 0) : minutes;
      this.hours = hours;
      this.minutes = minutes;
    },
  },
};
</script>

<template>
  <div class="taskbar" title="Start">
    <div class="start-button button">Start</div>
    <div class="task" id="task">Modal title</div>
    <div class="taskbar-time">
      <i class="devicon-react-original" title="View in React"></i>
      <i class="devicon-vuejs-plain" title="View in Vue"></i>
      <i class="devicon-angularjs-plain" title="View in Angular"></i>
      <i class="devicon-svelte-plain" title="View in Svelte"></i>
      <p class="taskbar-time-text" id="timetip">
        {{ hours }}:{{ minutes }}<span v-if="hours >= 13"> PM</span
        ><span v-else> AM</span>
      </p>
    </div>
  </div>

  <StartMenu />
</template>

<style scoped></style>
