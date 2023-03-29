<script>
export default {
  name: "Window",
  mounted() {
    // Active window
    document.querySelector(".task").addEventListener("click", function () {
      if (document.querySelector("#mainModal").css("display") == "flex") {
        document.querySelector("#mainModal").css("display", "none");
        document.querySelector(".task").css({
          border: "outset 2px",
          borderTop: "2px solid #deebf3",
          borderLeft: "2px solid #deebf3",
          borderRight: "2px solid black",
          borderBottom: "2px solid black",
        });
      } else {
        document.querySelector("#mainModal").css("display", "flex");
        document.querySelector(".task").css("border", "inset 2px");
      }
    });

    // Minimize window
    document.querySelector(".min").addEventListener("click", function () {
      document.querySelector("#mainModal").toggle();
      document.querySelector(".task").css({
        border: "outset 2px",
        borderTop: "2px solid #deebf3",
        borderLeft: "2px solid #deebf3",
        borderRight: "2px solid black",
        borderBottom: "2px solid black",
      });
    });

    // Maximize window
    document.querySelector(".max").addEventListener("click", function () {
      document.querySelector(".window").classList.toggle("maximize");
    });

    // Close window
    document
      .querySelector(".close, .ok")
      .addEventListener("click", function () {
        document.querySelector(".start-menu").css("display", "none");
        document.querySelector("#mainModal").css("display", "none");
        document.querySelector(".task").css("display", "none");
      });
  },
  methods: {
    // Handle window content
    openModal(myVal) {
      document.querySelector(".start-menu").css("display", "none");
      document.querySelector("#mainModal").find(".title").textContent = myVal;
      document.querySelector(".task").textContent = myVal;

      if (myVal === "About me") {
        document.querySelector(".content").innerHTML = `
        <div class='banner'></div>
        <hr>
        <p>About you here... 😄</p>
    `;
      }

      if (myVal === "My CV") {
        document.querySelector(".content").innerHTML =
          "<p>Your CV here... 😄</p>";
      }

      if (myVal === "My Portfolio") {
        document.querySelector(".content").innerHTML =
          "<p>Your Portfolio here... 😄</p>";
      }

      if (myVal === "App") {
        document.querySelector(".content").innerHTML = `
        <img src='https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg' width='30%' height='auto' />
        <p>Webdows 9.5 V.29.02</p>
        <hr>
        <p>JavaScript version (no frameworks). To view this app in framework versions (React, Vue, Angular and Svelte), simply click on Start, Shut down and select the preferred boot method. (Coming soon)</p>
        <hr>
      `;
      }

      document.querySelector("#mainModal").css("display", "flex");
      document.querySelector(".task").css("display", "block");
    },
  },
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
