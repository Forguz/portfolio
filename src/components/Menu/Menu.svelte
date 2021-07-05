<script>
  import { scale, slide } from 'svelte/transition'
  import { bounceOut } from 'svelte/easing';
  import Divider from '../../shared/Divider.svelte';
  import NavOption from '../../shared/NavOption.svelte';
  import MenuOption from './MenuOption.svelte';
</script>

<section out:scale={{duration: 1500, easing: bounceOut}} in:slide={{duration: 1500, easing: bounceOut}}>
  <div class="menu-content">
    <nav>
      <MenuOption>About</MenuOption>
      <MenuOption>Skills</MenuOption>
      <MenuOption>Projects</MenuOption>
      <MenuOption>Contact</MenuOption>
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