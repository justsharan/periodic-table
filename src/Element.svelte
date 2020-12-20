<script>
  export let atomic
  export let symbol
  export let name
  export let type
  export let atomic_mass
</script>

<section id={name.toLowerCase()} class={type}>
  <div id="atomic">{atomic}</div>
  <div id="symbol">{symbol}</div>
  <div id="name">{name}</div>
  <div id="mass">{Number.parseFloat(atomic_mass).toPrecision(3)}</div>
</section>

<style>

  section {
    width: 5vw;
    height: 5vw;
    padding: 2px;

    border: 0.5px solid;
    border-collapse: collapse;
    overflow: hidden;

    font-family: -apple-system, Helvetica, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    color: hsla(0,0%,100%,.55);
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

  #hafnium, #rutherfordium {
    grid-column-start: 4;
  }

  #space {
    grid-column-start: -2;
    border: none;
  }

  .alkali {
    background-color: rgba(114,47,61,.8);
  }

  .alkaline-earth {
    background-color: rgba(95,70,55,.8);
  }

  .transition {
    background-color: rgba(58,70,90,.8);
  }

  .post-transition {
    background-color: rgba(28,100,73,.8);
  }

  .metalloid {
    background-color: rgba(21,84,100,.8);
  }

  .nonmetal {
    background-color: rgba(77,74,150,.8);
  }

  .noble-gas {
    background-color: rgba(87,49,126,.8);
  }

  .lanthanide {
    background-color: rgba(74,57,110,.8);
  }

  .actinide {
    background-color: rgba(64,37,80,.8);
  }

</style>

