<script>
  export let atomic
  export let symbol
  export let name
</script>

<main id={name.toLowerCase()}>
  <div id="atomic">{atomic}</div>
  <div id="symbol">{symbol}</div>
  <div id="name">{name}</div>
</main>

<style>

  main {
    width: 5vw;
    height: 5vw;
    padding: 2px;

    border: 1px solid;
    border-collapse: collapse;
    overflow: hidden;

    font-family: -apple-system, Helvetica, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
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
    font-size: 2.5vw;
  }

  #name {
    font-size: 0.8vw;
    text-align: center;
  }

</style>

