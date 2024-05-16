<script setup>

</script>

<template>
  <h1>Float example</h1>

  <div class="wrapper">
    <div class="box">Float</div>

    <p class="special">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla luctus aliquam
      dolor, eu lacinia lorem placerat vulputate. Duis felis orci, pulvinar id metus
      ut, rutrum luctus orci. Cras porttitor imperdiet nunc, at ultricies tellus
      laoreet sit amet.
    </p>
  </div>
  
  <p class="cleared">
    Sed auctor cursus massa at porta. Integer ligula ipsum, tristique sit amet
    orci vel, viverra egestas ligula. Curabitur vehicula tellus neque, ac ornare
    ex malesuada et. In vitae convallis lacus. Aliquam erat volutpat. Suspendisse
    ac imperdiet turpis. Aenean finibus sollicitudin eros pharetra congue. Duis
    ornare egestas augue ut luctus. Proin blandit quam nec lacus varius commodo et
    a urna. Ut id ornare felis, eget fermentum sapien.
  </p>

  <p>
    Nam vulputate diam nec tempor bibendum. Donec luctus augue eget malesuada
    ultrices. Phasellus turpis est, posuere sit amet dapibus ut, facilisis sed
    est. Nam id risus quis ante semper consectetur eget aliquam lorem. Vivamus
    tristique elit dolor, sed pretium metus suscipit vel. Mauris ultricies lectus
    sed lobortis finibus. Vivamus eu urna eget velit cursus viverra quis
    vestibulum sem. Aliquam tincidunt eget purus in interdum. Cum sociis natoque
    penatibus et magnis dis parturient montes, nascetur ridiculus mus.
  </p>

  <div class="summary">
    <p>1.display:flow-root, this line of code is to create a BFC(Block Formatting Context). This is another way to perform similar effect of 'clear: xxx', this will make float element and other elements as long as they are inside 'display: flow-root' positioning like one Block Formatting Context.</p>
    <p>2.About BFC, you can refer to <a target="_blank" href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flow_layout/Block_and_inline_layout_in_normal_flow#elements_participating_in_an_inline_formatting_context">Block and Inline layout in normal flow</a> for more information.</p>
  </div>

</template>

<style scoped>
  body {
    width: 90%;
    max-width: 900px;
    margin: 0 auto;
    font:
      0.9em/1.2 Arial,
      Helvetica,
      sans-serif;
  }

  .box {
    float: left;
    margin-right: 15px;
    width: 150px;
    height: 100px;
    border-radius: 5px;
    background-color: rgb(207 232 220);
    padding: 1em;
  }
  
  .special {
    background-color: rgb(148 255 172);
    padding: 10px;
    color: purple;
  }

  .wrapper {
    background-color: rgb(148 255 172);
    padding: 10px;
    color: purple;
    display: flow-root;
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
  }
</style>