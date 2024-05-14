<script setup>

</script>

<template>
  <div class="container">
    <div>One</div>
    <div>Two</div>
    <div>Three</div>
    <div>Four</div>
    <div id="subgrid">
      <div>Five</div>
      <div>Six</div>
      <div>Seven</div>
      <div>Eight</div>
    </div>
    <div>Nine</div>
    <div>Ten</div>
  </div>
</template>

<!-- Positioning with grid-template-areas -->
<style scoped>
  div {
    background-color: rgb(207,232,220);
    border-radius: 5px;
    border: 2px solid rgb(79,185,227);
    padding: 10px;
  }

  /* add your CSS here */
  .container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(1, 1fr);
    gap: 10px;
  }

  #subgrid {
    grid-column: 1 / 4;
    grid-row: 2 / 4;
    display: grid;
    gap: inherit;
    grid-template-columns: subgrid;
    grid-template-rows: 2fr 1fr;
  }

</style>