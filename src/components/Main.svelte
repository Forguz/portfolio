<script>
  import { getContext, tick } from 'svelte';

  import Hamburguer from '../shared/Hamburguer.svelte';
  import LogoBox from '../shared/LogoBox.svelte';

  const { toggleMenu, isMenuVisible } = getContext('menu');
</script>

<main>
  <div class="menu-button">
    <Hamburguer on:click={toggleMenu} active={$isMenuVisible} />
  </div>
  <slot></slot>
  <div class="logo-box">
    <LogoBox />
  </div>
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
    z-index: 6;
    left: calc(100% - 48px - 80px);
    top: 88px;
  }
  .logo-box {
    position: absolute;
    top: auto;
    left: auto;
    right: 80px;
    bottom: 88px;
  }
</style>