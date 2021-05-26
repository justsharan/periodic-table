<script>
  import Element from './Element.svelte'
  const data = fetch('assets/data.json').then(d => d.json())
</script>

<main>

  {#await data}
    <br>
  {:then elements}
    {#each elements as el}
      <Element {...el} />
    {/each}
  {/await}

  <footer>
    ⭐️ me on <a href="https://github.com/sinistrecyborg/ptable" target="_blank">GitHub</a>
  </footer>

</main>

<style>

  main {
    display: grid;
    grid-template-columns: repeat(17, auto) 1fr;
    width: 90%;
    margin: 0 auto;
    font-family: -apple-system, Helvetica, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  footer {
    position: fixed;
    bottom: 2vw;
    right: 2vw;
    font-size: 1rem;
  }

  a:link, a:visited {
    text-decoration: underline;
    color: inherit;
  }

</style>

