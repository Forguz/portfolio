<script>
  import { slide } from 'svelte/transition'
  import NavOption from '../shared/NavOption.svelte';
</script>

<section transition:slide={{duration: 400}}>
  <div class="menu-content">
    <nav>
      <NavOption>About</NavOption>
      <NavOption>Skills</NavOption>
      <NavOption>Projects</NavOption>
      <NavOption>Contact</NavOption>
    </nav>
    <div></div>
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
</style>