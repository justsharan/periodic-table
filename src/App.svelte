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

</main>

<style>

main {
  display: grid;
  grid-template-columns: repeat(17, auto) 1fr;
  margin: 0 auto;
  font-family: -apple-system, Helvetica, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

</style>

