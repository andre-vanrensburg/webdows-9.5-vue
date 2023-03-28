<script>
export default {
  name: "Window",
};
</script>

<template>
  <div class="window" id="mainModal">
    <div class="titlebar">
      <span class="title"></span>
      <div class="titlebar-buttons">
        <div class="titlebar-button min">
          <i class="fa-solid fa-window-minimize"></i>
        </div>
        <div class="titlebar-button max">
          <i class="fa-sharp fa-regular fa-square"></i>
        </div>
        <div class="titlebar-button close">
          <i class="fa-solid fa-xmark"></i>
        </div>
      </div>
    </div>
    <div class="content-body">
      <div class="content"></div>
    </div>
    <div class="footer-buttons">
      <button class="button ok">OK</button>
    </div>
  </div>
</template>

<style scoped></style>
