<script>
export default {
  name: "StartMenu",
  mounted() {
    document
      .querySelector(".start-button")
      .addEventListener("click", function () {
        if (document.querySelector(".start-menu").css("display") == "none") {
          document.querySelector(".start-menu").css("display", "grid");
        } else {
          document.querySelector(".start-menu").css("display", "none");
        }
      });

    // Shutdown (Reload)
    document.querySelector(".shutdown").addEventListener("click", function () {
      location.reload();
    });

    document
      .querySelector(".start-menu-items ul a:not(#shutdown)")
      .addEventListener("click", function () {
        let myVal = document.querySelector(this).data("title");
        openModal(myVal);
      });
  },
};
</script>

<template>
  <div class="start-menu">
    <div class="start-menu-side">
      <div class="start-menu-side-text text">
        <p class="ninefive">9.5</p>
        <p class="windows">Webdows</p>
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"
          width="100%"
          height="auto"
        />
      </div>
    </div>

    <div class="start-menu-items">
      <ul class="start-menu-items-list1">
        <a
          class="start-menu-items-item-title"
          title="About me"
          data-title="About me"
          data-modal="#mainModal"
        >
          <li class="start-menu-items-item">
            <div class="icon">
              <img src="img/aboutme.png" width="100%" height="auto" />
            </div>
            <p>About <span class="underline">M</span>e</p>
          </li>
        </a>
        <a class="start-menu-items-item-title" data-title="My CV" title="My CV">
          <li class="start-menu-items-item">
            <div class="icon">
              <img src="img/cv.png" width="100%" height="auto" />
            </div>
            <p>My <span class="underline">C</span>V</p>
          </li>
        </a>
        <a
          class="start-menu-items-item-title"
          data-title="My Portfolio"
          title="My Portfolio"
        >
          <li class="start-menu-items-item">
            <div class="icon">
              <img src="img/portfolio.png" width="100%" height="auto" />
            </div>
            <p>My <span class="underline">P</span>ortfolio</p>
          </li>
        </a>
      </ul>

      <ul class="start-menu-items-list2">
        <a
          href="#"
          id="app"
          class="start-menu-items-item-title"
          title="App"
          data-title="App"
          data-modal="#mainModal"
        >
          <li class="start-menu-items-item">
            <div class="icon">
              <img src="img/about.png" width="100%" height="auto" />
            </div>
            <p><span class="underline">A</span>bout...</p>
          </li>
        </a>
        <a
          href="#"
          class="start-menu-items-item-title shutdown"
          title="Shut down"
          id="shutdown"
        >
          <li class="start-menu-items-item">
            <div class="icon">
              <img src="img/shutdown.png" width="100%" height="auto" />
            </div>
            <p>Sh<span class="underline">u</span>t Down...</p>
          </li>
        </a>
      </ul>
    </div>
  </div>
</template>

<style></style>
