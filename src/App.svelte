<script>
  import Element from './Element.svelte'

  const Hydrogen = {
    atomic: 1,
    symbol: "H",
    name: "Hydrogen"
  }

  const Helium = {
    atomic: 2,
    symbol: "He",
    name: "Helium"
  }
</script>

<main>

    <Element {...Hydrogen} />
    <Element {...Helium} />

</main>

<style>

  main {
    display: grid;
    grid-template-columns: repeat(17, auto) 1fr;
  }

</style>

