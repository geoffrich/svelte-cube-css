<script>
  import SiteHeader from "./SiteHeader.svelte";
  import KeyHeader from "./KeyHeader.svelte";
  import Summary from "./Summary.svelte";
  import TableGroup from "./TableGroup.svelte";
</script>

<style>

</style>

<SiteHeader />
<main>
  <article class="wrapper">
    <KeyHeader />
    <div class="[ splitter ] [ gap-top-600 ]">
      <TableGroup />
      <Summary balance={673.43} outgoings={874.88} income={1548.31} />
    </div>
  </article>
</main>
