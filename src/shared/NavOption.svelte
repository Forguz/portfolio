<script>
  export let shadowColor;
</script>

<a href="#">
  <slot />
</a>

<style>
  a {
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--background-color);
    font-size: 4.8rem;
    text-decoration: none;
    font-weight: 500;
  }
</style>