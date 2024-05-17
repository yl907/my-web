<script setup>
  import longImage from '@/assets/long.jpg'
</script>

<template>
  <div id="fixedPositioning">
    
    <div class="fixed">this is a fixed positioning element, <a href="#fixedPositioning">go to fixed positioning part</a></div>

    <div class="main-content">As you can see at top right corner, it is a fixed positioning element.</div>

    <div class="summary">
      <p>1.'position: fixed;' will make the element to be fixed at this page.</p>
      <p>2.use 'top/right/bottom/left: xx;' to specify specific position.</p>
    </div>
    
  </div>
</template>

<style scoped>
  body {
    width: 500px;
    margin: 0 auto;
  }

  p {
    background: aqua;
    border: 3px solid blue;
    padding: 10px;
    margin: 10px;
  }

  span {
    background: red;
    border: 1px solid black;
  }

  a {
    text-decoration: underline;
  }

  a:hover {
    text-decoration: none;
  }

  .fixed {
    position: fixed;
    top: 0px;
    right:0px;
    border: 1px black solid;
    background-color: gainsboro;
    padding: 2px;
  }

  .main-content {
    font-size: 1.5em;
  }

  .summary {
    color: white;
    background-color: rgba(18, 17, 22, 0.733);
    border-radius: 2em;
    padding-top: 1em; padding-bottom: 1em;  padding-left: 2em; padding-right: 2em;
    border: 1px solid;
    margin: 1em;
    width: fit-content;

    p {
      background: none;
      border: none;
      padding: none;
      margin: none;
    }
  }

</style>