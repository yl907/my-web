<script setup>

</script>

<template>
  <div class="container">
    <header>This is my lovely blog<span>(column:1/3, row:1)</span></header>
    <article>
      <h1>My article<span>(column:2, row:2)</span></h1>
      <p>
        Duis felis orci, pulvinar id metus ut, rutrum luctus orci. Cras
        porttitor imperdiet nunc, at ultricies tellus laoreet sit amet. Sed
        auctor cursus massa at porta. Integer ligula ipsum, tristique sit amet
        orci vel, viverra egestas ligula. Curabitur vehicula tellus neque, ac
        ornare ex malesuada et. In vitae convallis lacus. Aliquam erat
        volutpat. Suspendisse ac imperdiet turpis. Aenean finibus sollicitudin
        eros pharetra congue. Duis ornare egestas augue ut luctus. Proin
        blandit quam nec lacus varius commodo et a urna. Ut id ornare felis,
        eget fermentum sapien.
      </p>

      <p>
        Nam vulputate diam nec tempor bibendum. Donec luctus augue eget
        malesuada ultrices. Phasellus turpis est, posuere sit amet dapibus ut,
        facilisis sed est. Nam id risus quis ante semper consectetur eget
        aliquam lorem. Vivamus tristique elit dolor, sed pretium metus
        suscipit vel. Mauris ultricies lectus sed lobortis finibus. Vivamus eu
        urna eget velit cursus viverra quis vestibulum sem. Aliquam tincidunt
        eget purus in interdum. Cum sociis natoque penatibus et magnis dis
        parturient montes, nascetur ridiculus mus.
      </p>
    </article>
    <aside>
      <h2>
        Other things <br />
        <span>(column:1, row:2)</span>
      </h2>
      <p>
        Nam vulputate diam nec tempor bibendum. Donec luctus augue eget
        malesuada ultrices. Phasellus turpis est, posuere sit amet dapibus ut,
        facilisis sed est.
      </p>
    </aside>
    <footer>Contact me@mysite.com<span>(column: 1/3, row:3)</span></footer>
  </div>

  <div class="summary">
    <p>1.grid-column: 1/3; 表示该grid item占用了第[1, 3)列。</p>
    <p>1.grid-row: 2; 表示该grid item占用了第2行。</p>
  </div>
</template>

<!-- Line-based placement -->
<style scoped>
  body {
    width: 90%;
    max-width: 900px;
    margin: 2em auto;
    font: 0.9em/1.2 Arial, Helvetica, sans-serif;
  }

  .container {
    display: grid;
    grid-template-columns: 1fr 3fr;
    gap: 20px;
  }

  header,
  footer {
    border-radius: 5px;
    padding: 10px;
    background-color: rgb(207, 232, 220);
    border: 2px solid rgb(79, 185, 227);
  }

  aside {
    border-right: 1px solid #999;
  }

  /* add your CSS here */
  header {
    grid-column: 1 / 3;
    grid-row: 1;
  }

  article {
    grid-column: 2;
    grid-row: 2;
  }

  aside {
    grid-column: 1;
    grid-row: 2;
  }

  footer {
    grid-column: 1 / 3;
    grid-row: 3;
  }

  span {
    color: grey;
    text-decoration: underline;
    font-weight: bolder;
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