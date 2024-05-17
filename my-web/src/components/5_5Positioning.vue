<script setup>
  import longImage from '@/assets/long.jpg'
</script>

<template>
  <div id="stickyPositioning">
    <div class="sticky">this is a sticky positioning element, <a href="#stickyPositioning">go to sticky positioning part</a></div>

    <div class="main-content">Sticky element initially act like a static element, but when reach a certain point, it will fixed at the page, then act like a fixed element.</div>

    <div>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
      <p>Some content here to make the page scrollable...</p>
    </div>

    <div class="summary">
      <p>1.position: absolute的元素位置是相对于containing block/containing element而言的，如果想了解containing block可以参考<a target="_blank" href="https://developer.mozilla.org/en-US/docs/Web/CSS/Containing_block#identifying_the_containing_block">Identifying the contaning block</a>.</p>
    </div>
  </div>

</template>

<style scoped>
  body {
    width: 500px;
    margin: 0 auto;
  }

  p {
    margin: 40px;
  }

  span {
    background: red;
    border: 1px solid black;
  }

  /* make this class element to be BFC */
  .BFC {
    position: relative;
  }

  .sticky {
    position: sticky;
    top: 0px;
    left: 0px;
    width: fit-content;
    border: 1px black solid;
    background-color: gainsboro;
    padding: 2px;
  }

  a {
    text-decoration: underline;
  }

  a:hover {
    text-decoration: none;
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