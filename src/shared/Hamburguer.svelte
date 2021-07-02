<script>
  export let active = false;
</script>

<button on:click class:active></button>

<style>
  button {
    width: 48px;
    color: var(--primary-color);
    z-index: inherit;
    background-color: transparent;
    border-top: 8px solid currentColor;
    transition: 400ms;
  }
  
  button::before, button::after {
    content: '';
    display: block;
    width: 48px;
    height: 8px;
    background-color: currentColor;
    margin-top: 8px;
    transition: transform 400ms;
    position: relative;
  }

  .active {
    border-top: transparent;
    color: var(--background-color);
  }

  .active::before {
    transform: rotate(135deg);
  }

  .active::after {
    transform: rotate(-135deg);
    top: -15px;
  }
</style>