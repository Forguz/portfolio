<script>
  export let active = false;
</script>

<button on:click class:active></button>

<style>
  button {
    width: 48px;
    color: var(--primary-color);
    border-top: 8px solid currentColor;
    transition: 300ms;
  }
  
  button::before, button::after {
    content: '';
    display: block;
    width: 48px;
    height: 8px;
    background-color: currentColor;
    margin-top: 8px;
    transition: transform 300ms;
    position: relative;
  }

  .active {
    border-top: transparent;
  }

  .active::before {
    transform: rotate(135deg);
  }

  .active::after {
    transform: rotate(-135deg);
    top: -15px;
  }
</style>