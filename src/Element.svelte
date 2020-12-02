<script>
  export let atomic
  export let symbol
  export let name
  export let atomic_mass
</script>

<main id={name.toLowerCase()}>
  <div id="atomic">{atomic}</div>
  <div id="symbol">{symbol}</div>
  <div id="name">{name}</div>
  <div id="mass">{Number.parseFloat(atomic_mass).toPrecision(3)}</div>
</main>

<style>

  main {
    width: 5vw;
    height: 5vw;
    padding: 2px;

    border: 0.5px solid;
    border-collapse: collapse;
    overflow: hidden;

    font-family: -apple-system, Helvetica, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    color: #eeeeee;
  }

  #atomic {
    float: left;
    font-size: 0.5vw;
    position: absolute;
  }

  #symbol {
    font-weight: bold;
    text-align: center;
    margin-top: 0.5vw;
    font-size: 2vw;
  }

  #name {
    font-size: 0.8vw;
    text-align: center;
  }

  #mass {
    font-size: 0.625vw;
    text-align: center;
  }

  #helium {
    grid-column-start: -2;
  }

  #boron, #aluminium {
    grid-column-start: 13;
  }

  #lanthanum, #actinium {
    grid-column-start: 3;
  }

  #empty {
    border: none;
  }

  #empty > div, #space > div {
    color: #1c1c1c;
  }

  #space {
    grid-column-start: -2;
    border: none;
  }

</style>

