<script setup>
  import longImage from '@/assets/long.jpg';
</script>

<template>
  <div class="BFC">
    <h1>Introducing z-index</h1>

    <p class="main-content">I am a basic block level element. My adjacent block level elements sit on new lines below me.</p>

    <p class="main-content positioned">By default we span 100% of the width of our parent element, and our are as tall as our child content. Our total width and height is our content + padding + border width/height.</p>

    <p class="main-content">We are separated by our margins. Because of margin collapsing, we are separated by the width of one of our margins, not both.</p>

    <p class="main-content">inline elements <span>like this one</span> and <span>this one</span> sit on the same line as one another, and adjacent text nodes, if there is space on the same line. Overflowing inline elements <span>wrap onto a new line if possible — like this one containing text</span>, or just go on to a new line if not, much like this image will do: <img :src="longImage" alt="a wide but short section of a photo of several fabrics"></p>
  </div>

  <div class="summary">
    <p>1.'z-index: xx;' determines which elements is appear over others and which elements appear under others. </p>
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

  div.BFC {
    /* make this element a 'block formatting contexts' */
    position: relative;
  }

  .positioned {
    position: absolute;
    top: 30px;
    left: 30px;
    background: yellow;
  }

  p.main-content:nth-of-type(1) {
    /* try comment out below one line of code, and see the effect. */
    z-index: 1;
    position: absolute;
    background: lime;
    top: 10px;
    right: 30px;
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