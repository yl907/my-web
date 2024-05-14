<script setup>

</script>

<template>
  <h1>Simple grid example</h1>
  <div class="gridContainer">
      <div>One</div>
      <div>Two</div>
      <div>Three</div>
      <div>Four</div>
      <div>Five</div>
      <div>Six</div>
      <div>Seven</div>
  </div>
</template>

<style scoped>
  body {
      width: 90%;
      max-width: 900px;
      margin: 2em auto;
      font: .9em/1.2 Arial, Helvetica, sans-serif;
  }

  .gridContainer > div {
      border-radius: 5px;
      padding: 10px;
      background-color: rgb(207,232,220);
      border: 2px solid rgb(79,185,227);
  }
  
  /* add your CSS here */
  .gridContainer {
    display: grid;
    
    /* version1: */
    /* grid-template-columns: 200px 200px 200px; */

    /* version2: */
    /* grid-template-columns: 2fr 1fr 1fr; */

    /* version3: */
    /* grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: 100px; */
    
    /* version4: */
    /* grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: minmax(100px, auto); */

    /* version5(As many columns as will fit): */
    --minimal-width: 200px;
    grid-template-columns: repeat(auto-fit, minmax(var(--minimal-width), 1fr));
    grid-auto-rows: minmax(100px, auto);

    gap: 20px;
  }
</style>