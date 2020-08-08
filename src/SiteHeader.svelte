<script>
  import User from "./User.svelte";
</script>

<style lang="scss">
  .site-head {
    padding: 0.4rem 0 0.8rem 0;

    &__inner {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
    }
  }

  // Right margin prevents any collisions with the title
  h1 {
    margin: 0.5rem 1rem 0.5rem 0;
  }
</style>

<header role="banner" class="[ site-head ] [ bg-tertiary-glare ]">
  <div class="wrapper">
    <div class="site-head__inner">
      <h1 class="text-600">Account overview</h1>
      <User />
    </div>
  </div>
</header>
