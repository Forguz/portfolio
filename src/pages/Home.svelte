<script>
  import LogoBox from '../shared/LogoBox.svelte';
  import Divider from '../shared/Divider.svelte';
</script>

<section>
  <h1>
    Hello! <br>
    I’m <span>Nícolas Dellazzeri</span>,
    a Web Developer and Design enthusiast.
  </h1>
  <Divider --type="dashed" --width="62.4rem" --margin-top="2.4rem" />
  <!-- <div class="divider"></div> -->
  <footer>
    <h3>
      Actually working at <span>amcom</span>
      as a software developer
    </h3>
  </footer>
</section>

<style>
  section {
    padding: 88px;
    padding-right: 80px;
  }
  h1 {
    font-weight: 700;
    font-size: 7.2rem;
    line-height: 107%;
    letter-spacing: 0.025em;
    max-width: 696px;
  }
  span {
    color: var(--primary-color);
  }
  footer {
    display: flex;
    justify-content: space-between;
  }
  h3 {
    font-size: 4.8rem;
    max-width: 51.1rem;
    line-height: 104%;
    letter-spacing: -0.025em;
    margin-top: 24px;
  }
</style>