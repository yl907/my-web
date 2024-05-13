<script setup>

</script>

<template>
  <div class="container">
    <button>Smile</button>
    <button>Laugh</button>
    <button>Wink</button>
    <button>Shrug</button>
    <button>Blush</button>
  </div>

  <div class="summary">
    <p>1.align-items: center; 专门用于flexbox和grid layout的属性, 其值有start/center/end, 对应的是cross axis方向.</p>
    <p>2.justify-content: space-around; 同样是专门用于flex和grid容器的属性, 对应的是main axis方向.</p>
  </div>
</template>

<style scoped>
  html {
    font-family: sans-serif;
  }

  body {
    width: 70%;
    max-width: 960px;
    margin: 20px auto;
  }

  button {
    font-size: 18px;
    line-height: 1.5;
    width: 15%;
  }

  div {
    height: 100px;
    border: 1px solid black;
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

  /* Add your flexbox CSS below here */
  div.container {
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    justify-content: space-around;
  }

</style>