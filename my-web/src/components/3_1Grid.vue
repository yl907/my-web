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

  <div class="summary">
    <p>1.为每列的宽度设置固定的值： grid-template-columns: 200px 200px 200px;</p>
    <p>2.使用fr作为列宽度的值，每个fr会使用当前页面剩余空间的一个单位长度：grid-template-columns: 2fr 1fr 1fr;(长度之比为2:1:1, 且这三个列会占用全部可用空间)</p>
    <p>3.简写：grid-template-columns: repeat(3, 1fr);</p>
    <p>4.minmax()用于行宽度，此处使用 minmax(100px, auto) 的好处有许多，比如：<br />
      4.1.最小高度保证: 100px 作为最小高度，确保每一行至少有 100px 的高度，不会小于这个值。这对排版整齐、视觉一致性很重要，特别是在某些内容较少的行中。<br />
      4.2.高度自适应: auto 作为最大高度，允许行根据内容自动调整高度。这样，如果行内的内容高度超过 100px，行会自动扩展以容纳内容，而不会截断内容。<br />
      4.3.更好的布局控制: 使用 minmax 可以更灵活地控制布局，使其既能满足最小高度要求，又能根据内容灵活调整。这种方式适用于需要动态调整行高的布局，例如内容高度变化较大的情况下。<br />
      4.4.避免内容溢出: 通过设置最大高度为 auto，可以防止内容溢出行框，从而避免出现滚动条或者内容被裁剪的问题。
    </p>
    <p>5.minmax()用于列宽度，搭配auto-fit可以实现尽可能多的插入列：<br />
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));<br />
      grid-auto-rows: minmax(100px, auto);
    </p>
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