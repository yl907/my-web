<script setup>

</script>

<template>
  <div class="container">
      <h1>multicol: three-column</h1>

      <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla luctus aliquam dolor, eu lacinia lorem placerat vulputate.
          Duis felis orci, pulvinar id metus ut, rutrum luctus orci. Cras porttitor imperdiet nunc, at ultricies tellus
          laoreet sit amet. Sed auctor cursus massa at porta. Integer ligula ipsum, tristique sit amet orci vel, viverra
          egestas ligula. Curabitur vehicula tellus neque, ac ornare ex malesuada et. In vitae convallis lacus. Aliquam
          erat volutpat. Suspendisse ac imperdiet turpis. Aenean finibus sollicitudin eros pharetra congue. Duis ornare
          egestas augue ut luctus. Proin blandit quam nec lacus varius commodo et a urna. Ut id ornare felis, eget fermentum
          sapien.</p>

      <p>Nam vulputate diam nec tempor bibendum. Donec luctus augue eget malesuada ultrices. Phasellus turpis est, posuere
          sit amet dapibus ut, facilisis sed est. Nam id risus quis ante semper consectetur eget aliquam lorem. Vivamus
          tristique elit dolor, sed pretium metus suscipit vel. Mauris ultricies lectus sed lobortis finibus. Vivamus eu
          urna eget velit cursus viverra quis vestibulum sem. Aliquam tincidunt eget purus in interdum. Cum sociis natoque
          penatibus et magnis dis parturient montes, nascetur ridiculus mus.</p>
  </div>

  <div class="summary">
    <p>1.'column-count: 3': specify this is a 3 column layout.</p>
    <p>2.'column-gap: 20px': control gap width.</p>
    <p>3.'column-rule: 4px dotted rgb(xx xx xx)': create a line in every gap, which is 4px dotted rgb(xx xx xx).</p>
  </div>
</template>

<style scoped>
  .container {
    /* A three-column layout */
    column-count: 3;
    /* Styling gaps */
    column-gap: 20px;
    column-rule: 4px dotted rgb(79 185 227);
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