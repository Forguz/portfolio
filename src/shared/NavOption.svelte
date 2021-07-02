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
    /* background-color: var(--primary-color); */
    color: var(--background-color);
    font-size: 6.4rem;
    text-decoration: none;
    font-weight: 500;
    margin-bottom: 56px;
  }
</style>