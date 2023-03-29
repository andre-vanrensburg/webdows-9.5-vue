<script>
export default {
  name: "Boot",
  mounted() {
    // Handle bootscreen
    setTimeout(function () {
      document.querySelector("#boot").style.display = "none";
    }, 2000);
  },
};
</script>

<template>
  <div id="boot">
    <div>
      <p>
        System Configuration (c) 1998 - 2023 WebDos (Web Disk Operating System
        [Version 19.87]), <br />
        Andre van Rensburg. All rights reserved.
      </p>
      <br />
      <p>
        Intel 80386SX CPU at 40MHz<br />
        Memory Test : 42291000KB<br />
        Detecting IDE Primary Master : Local Storage<br />
        Detecting IDE Primary Slave : None<br />
        Detecting IDE Secondary Master : None<br />
        Detecting IDE Secondary Slave : None
      </p>
    </div>

    <div>
      <img src="../assets/es.png" data-credit="Property of ENERGY STAR&#174;" />
    </div>

    <div class="footer">
      <p>
        Press Del to enter setup.<br />
        15/04/87-dsakd32r.43834ksa.134931
      </p>
    </div>
  </div>
</template>
