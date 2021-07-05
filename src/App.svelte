<script>
  import { getContext, onMount, setContext } from 'svelte';

  import { isMenuVisible } from './stores/menu';

  import Main from './components/Main.svelte';
  import Menu from './components/Menu/Menu.svelte';
  import Home from './pages/Home.svelte';

  function toggleMenu() {
    $isMenuVisible = !$isMenuVisible;
  }

  setContext('menu', {
    toggleMenu,
    isMenuVisible
  });

</script>

{#if $isMenuVisible}
  <Menu />
{/if}
<div>
  <Main>
    <Home />
  </Main>
</div>

<style>
  div {
    height: 100%;
    padding: 48px;
    padding-left: 64px;
  }
</style>