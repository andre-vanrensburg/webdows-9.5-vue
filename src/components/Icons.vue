<script>
export default {
  name: "Icons",
};
</script>

<template>
  <div
    class="icon-content about"
    title="About me"
    data-title="About me"
    data-modal="#mainModal"
  >
    <img
      src="../assets/aboutme.png"
      width="50px"
      height="50px"
      data-title="About me"
    />
    <a data-title="About me">About Me</a>
  </div>

  <div
    class="icon-content cv"
    title="My CV"
    data-title="My CV"
    data-modal="#mainModal"
  >
    <img src="../assets/cv.png" width="50px" height="50px" data-title="My CV" />
    <a data-title="My CV">My CV</a>
  </div>

  <div
    class="icon-content portfolio"
    title="My Portfolio"
    data-title="My Portfolio"
    data-modal="#mainModal"
  >
    <img
      src="../assets/portfolio.png"
      width="50px"
      height="50px"
      data-title="My Portfolio"
    />
    <a data-title="My Portfolio">My Portfolio</a>
  </div>
</template>

<style></style>
