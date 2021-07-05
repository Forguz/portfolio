
<!-- <div class="container">
  <div class="shadow" /> -->
  <a href="" on:click|preventDefault>
    <slot></slot>
  </a>
<!-- </div> -->

<style>
  .container {
    display: flex;
    position: relative;
  }
  a {
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--background-color);
    font-size: 4.8rem;
    text-decoration: none;
    font-weight: 500;
    cursor: pointer;
    border: .8rem solid transparent;
    padding: 2.4rem;
    transition: ease 150ms all;
  }

  a:hover {
    transform: translate(10px, -10px);
    border-color: var(--background-color);
    box-shadow: 0px 8px var(--background-color), -8px 0px var(--background-color), -8px 8px var(--background-color);
  }

  a:active {
    transform: translate(0px, 0px);
    box-shadow: none;
  }
</style>