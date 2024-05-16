<script setup>
  import longImage from '@/assets/long.jpg'
</script>

<template>
  <div class="containingElement">
    <h1>Absolute positioning</h1>

    <p>I am a basic block level element. My adjacent block level elements sit on new lines below me.</p>

    <p class="positioned">By default we span 100% of the width of our parent element, and our are as tall as our child content. Our total width and height is our content + padding + border width/height.</p>

    <p>We are separated by our margins. Because of margin collapsing, we are separated by the width of one of our margins, not both.</p>

    <p>inline elements <span>like this one</span> and <span>this one</span> sit on the same line as one another, and adjacent text nodes, if there is space on the same line. Overflowing inline elements <span>wrap onto a new line if possible — like this one containing text</span>, or just go on to a new line if not, much like this image will do: <img :src="longImage" alt="a wide but short section of a photo of several fabrics"></p>
  </div>

  <div class="summary">
    <p>1.position: absolute的元素位置是相对于containing block/containing element而言的，如果想了解containing block可以参考<a target="_blank" href="https://developer.mozilla.org/en-US/docs/Web/CSS/Containing_block#identifying_the_containing_block">Identifying the contaning block</a>.</p>
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

  /* make this class element to be Positioning contexts */
  .containingElement {
    position: relative;
  }

  .positioned {
    position: absolute;
    top: 30px;
    left: 30px;
    background: yellow;
  }

  a {
    color: white;
    text-decoration: underline;
  }

  a:hover {
    text-decoration: none;
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