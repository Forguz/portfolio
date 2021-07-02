<script>
  import { scale, slide } from 'svelte/transition'
  import { bounceOut } from 'svelte/easing';
  import Divider from '../shared/Divider.svelte';
  import NavOption from '../shared/NavOption.svelte';
</script>

<section out:scale={{duration: 1500, easing: bounceOut}} in:slide={{duration: 1500, easing: bounceOut}}>
  <div class="menu-content">
    <nav>
      <a>About</a>
      <a>Skills</a>
      <a>Projects</a>
      <a>Contact</a>
    </nav>
    <Divider 
      --type="solid"
      --font-color="#f4e4e4"
      --width="30rem"
      --margin-top="5.6rem" />
    <div class="language-box">
      <NavOption>EN</NavOption>
      <NavOption>PT</NavOption>
    </div>
  </div>
</section>

<style>
  section {
    z-index: 5;
    position: fixed;
    width: 100vw;
    height: 100vh;
    background-color: var(--primary-color);
    padding: 48px;
    padding-left: 64px;
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
  }
  nav > a + a {
    margin-top: 4.8rem;
  }
  .menu-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 8px solid var(--background-color);
    width: 100%;
    height: 100%;
  }
  .language-box {
    margin-top: 2.4rem;
    display: flex;
    width: 14rem;
    justify-content: space-between;
  }
</style>