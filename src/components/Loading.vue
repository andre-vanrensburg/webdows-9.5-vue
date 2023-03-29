<script>
export default {
  name: "Loading",
  mounted() {
    setTimeout(function () {
      document.querySelector("#loading").style.display = "none";
      document.querySelector("#welcome")[0].play();
    }, 8000);
  },
};
</script>

<template>
  <div id="loading"></div>
</template>
