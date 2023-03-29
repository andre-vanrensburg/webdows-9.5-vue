<script>
export default {
  name: "Prompt",
  mounted() {
    typeWriter();
    setTimeout(function () {
      document.querySelector("#prompt").style.display = "none";
      document.querySelector("#prompt").dbladdEventListener("click");
    }, 5000);
  },
  data() {
    return {
      i: 0,
      txt: "start",
      speed: 150,
    };
  },
  methods: {
    typeWriter() {
      if (i < txt.length) {
        document.getElementById("key").value += txt.charAt(i);
        i++;
        setTimeout(typeWriter, speed);
      }
    },
  },
};
</script>

<template>
  <div id="prompt">
    <table class="table">
      <tr>
        <th colspan="2">
          System Configuration (c) 1998 - 2023 WebDos (Web disk Operating System
          [Version 19.87]), Andre van Rensburg. All rights reserved.
        </th>
      </tr>
      <tr>
        <td>Main Processor: 80386SX</td>
        <td>Base Memory Size: 42291000KB</td>
      </tr>
      <tr rowspan="2">
        <td>Numeric Processor: 80387SX</td>
        <td>Extended Memory Size: 1408KB</td>
      </tr>
      <tr rowspan="2">
        <td>Cache Size: 64KB</td>
        <td>Hard Disk Type: Local Storage</td>
      </tr>
      <tr rowspan="2">
        <td>BIOS Date: 15/04/87</td>
        <td>Display Type: VGA</td>
      </tr>
    </table>
    <div>
      <p>Type "start" and hit enter to start Webdows 9.5</p>
      <p>WebDos:\><input type="text" name="key" id="key" autofocus /></p>
    </div>
  </div>
</template>
