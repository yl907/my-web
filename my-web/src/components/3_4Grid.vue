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

  <div class="summary">
    <p>整体上subgrid并没有什么地方与grid不同，仅仅是嵌套的grid。但有几个属性存在特殊值，具体如下：</p>
    <p>gap: inherit;  使subgrid继承parent grid的间隔。</p>
    <p>grid-template-columns: subgrid;  使subgrid继承parent grid的列分布。</p>
    <p>从实际的subgrid效果上可以看出上述两个subgrid独有属性值都是为了parent grid和subgrid的一致性而存在的，继承列分布和间隔后，subgrid中的元素就好像跟外部grid的元素对齐了一样。</p>
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

  .summary {
    color: white;
    background-color: rgba(18, 17, 22, 0.733);
    border-radius: 2em;
    padding-top: 1em; padding-bottom: 1em;  padding-left: 2em; padding-right: 2em;
    border: 1px solid;
    margin: 1em;
    width: fit-content;
  }
</style>