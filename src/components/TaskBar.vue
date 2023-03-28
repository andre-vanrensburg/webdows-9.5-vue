<script>
import StartMenu from "./StartMenu.vue";

// // Time tooltip
// var timeTip = new Date().toLocaleDateString();
// document.getElementById("timetip").setAttribute("title", timeTip);

// // Clock
// function startTime() {
//   var today = new Date();
//   var h = today.getHours();
//   var m = today.getMinutes();
//   var s = today.getSeconds();
//   // add a zero in front of numbers<10
//   m = checkTime(m);
//   s = checkTime(s);
//   var hd = h;
//   $("#timetip").html(
//     (hd = 0 ? "12" : hd > 12 ? hd - 12 : hd) +
//       ":" +
//       m +
//       " " +
//       (h < 12 ? "AM" : "PM")
//   );
//   t = setTimeout(function () {
//     startTime();
//   }, 500);
// }

// function checkTime(i) {
//   if (i < 10) {
//     i = "0" + i;
//   }
//   return i;
// }

// startTime();

// export default {
//   name: "TaskBar",
//   components: {
//     name: StartMenu,
//   },
// };
//
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
      <p class="taskbar-time-text" id="timetip"></p>
    </div>
  </div>

  <StartMenu />
</template>

<style scoped></style>
