<script>
  import Logo from './assets/Logo.svelte';
</script>
<div class="box">
  <div class="backdrop"></div>
  <button class="logo">
    <Logo />
  </button>
</div>

<style>
  .box {
    display: flex;
  }
  .backdrop {
    position: relative;
    background-color: var(--primary-color);
    width: 268px;
    height: 242px;
    left: calc(268px - 12px);
    top: calc(20px + 12px);
  }
  .logo {
    box-sizing: initial;
    z-index: 1;
    background-color: var(--background-color);
    margin-top: 20px;
    padding: 12px;
    box-shadow: 0px 4px 6px 0px #00000040,0px 4px 4px 0px #00000040;
    border: 8px solid var(--font-color);
    transition: linear transform 50ms;
    cursor: pointer;
  }
  .logo:active {
    transform: translate(-12px, 12px);
  }
</style>