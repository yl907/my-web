<script setup>

</script>

<template>
  <div class="wrapper">
    <header>
      <nav>
        <ul>
          <li><a href="">About</a></li>
          <li><a href="">Contact</a></li>
          <li><a href="">Meet the team</a></li>
          <li><a href="">Blog</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <article>
        <div class="content">
          <h1>Veggies!</h1>
          <p>…</p>
        </div>
        <aside class="related">
          <p>…</p>
        </aside>
      </article>

      <aside class="sidebar">
        <h2>External vegetable-based links</h2>
        <ul>
          <li>…</li>
        </ul>
      </aside>
    </main>

    <footer><p>&copy;2019</p></footer>
  </div>

</template>

<style scoped>
  /* LAYOUT 1 */
  * {
    box-sizing: border-box;
  }

  body {
    width: 90%;
    margin: 2em auto;
    font:
      1em/1.3 Arial,
      Helvetica,
      sans-serif;
  }

  a:link,
  a:visited {
    color: #333;
  }

  nav ul,
  aside ul {
    list-style: none;
    padding: 0;
  }

  nav a:link,
  nav a:visited {
    background-color: rgb(207 232 220 / 20%);
    border: 2px solid rgb(79 185 227);
    text-decoration: none;
    display: block;
    padding: 10px;
    color: #333;
    font-weight: bold;
  }

  nav a:hover {
    background-color: rgb(207 232 220 / 70%);
  }

  .related {
    background-color: rgb(79 185 227 / 30%);
    border: 1px solid rgb(79 185 227);
    padding: 10px;
  }

  .sidebar {
    background-color: rgb(207 232 220 / 50%);
    padding: 10px;
  }

  article {
    margin-bottom: 1em;
  }

  /* add you CSS here */
  /* LAYOUT 2 */
  @media screen and (min-width: 40em) {
    article {
      display: grid;
      grid-template-columns: 3fr 1fr;
      column-gap: 20px;
    }

    nav ul {
      display: flex;
    }

    nav li {
      flex: 1;
    }
  }

  /* LAYOUT 3 */
  @media screen and (min-width: 70em) {
  main {
    display: grid;
    grid-template-columns: 3fr 1fr;
    column-gap: 20px;
  }

  article {
    margin-bottom: 0;
  }

  footer {
    border-top: 1px solid #ccc;
    margin-top: 2em;
  }
}

</style>
