<script>
  import Button from "./Button.svelte";
</script>

<style lang="scss">
  @import "../scss/helpers";

  .key-header {
    align-items: flex-end;

    > :last-child {
      display: flex;
      flex-wrap: wrap;
      gap: get-size("300");

      > * {
        flex-shrink: 0;
        margin: 0.2rem 0 0 0.2rem;
      }
    }

    @include media-query("md") {
      > :last-child {
        justify-content: flex-end;
      }
    }
  }
</style>

<div class="[ key-header ] [ splitter ] [ gap-top-700 ]">
  <h2 class="text-700" id="transaction-label">Latest transactions</h2>
  <aside>
    <Button href="#" variant="ghost">Get statement</Button>
    <Button href="#">Make payment</Button>
  </aside>
</div>
