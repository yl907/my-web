<script setup>

</script>

<template>
  <div class="container">
    <header>This is my lovely blog<span>(area-nickname:header)</span></header>
    <article>
      <h1>My article<span>(area-nickname:content)</span></h1>
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
        <span>area-nickname:sidebar</span>
      </h2>
      <p>
        Nam vulputate diam nec tempor bibendum. Donec luctus augue eget
        malesuada ultrices. Phasellus turpis est, posuere sit amet dapibus ut,
        facilisis sed est.
      </p>
    </aside>
    <footer>Contact me@mysite.com<span>(area-nickname:footer)</span></footer>
  </div>

  <div class="summary">
    <p>在grid container中指定m行n列的grid item是什么名字，然后在grid item中给当前元素进行命名，这个名字专门用于grid.</p>

    <p>
      比如有一个grid container中的各行各列按如下划分：<br />
      grid-template-areas:<br />
      "header header"<br />
      "sidebar content"<br />
      "footer footer";
    </p>

    <p>有一个grid item进行如下命名：<br />
      grid-area: header;</p>
  </div>
</template>

<!-- Positioning with grid-template-areas -->
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

  /* add your CSS here */
  .container {
    display: grid;
    grid-template-areas:
      "header header"
      "sidebar content"
      "footer footer";
    grid-template-columns: 1fr 3fr;
    gap: 20px;
  }

  header {
    /* grid-area: header; 
    this 'header' here can be anything else, if they match something in the 'grid-template-area', 
    So this 'header' here is like a nickname, which is used to specify specific things.*/
    grid-area: header;
  }

  article {
    grid-area: content;
  }

  aside {
    grid-area: sidebar;
  }

  footer {
    grid-area: footer;
  }

  aside {
    border-right: 1px solid #999;
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