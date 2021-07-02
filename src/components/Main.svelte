<script>
  import Hamburguer from '../shared/Hamburguer.svelte';
  let active = false;

  function toggleActive(event) {
    console.log(event.type);
    // if (event.type === 'touchstart') event.preventDefault();
    active = !active;
  }
</script>

<main>
  <div class="menu-button">
    <Hamburguer on:click={toggleActive} on:touch={toggleActive} {active} />
  </div>
  <slot></slot>
</main>

<style>
  main {
    position: relative;
    height: 100%;
    border: 8px solid var(--font-color);
    box-shadow: -16px 16px 0px 0px #A91212;
  }
  .menu-button {
    position: absolute;
    left: calc(100% - 48px - 80px);
    top: 88px;
  }
</style>