<script>
  export let balance, outgoings, income;
</script>

<style lang="scss">
  @import "../scss/helpers";
  .summary {
    padding: get-size("500") get-size("500") get-size("600") get-size("500");
    line-height: 1.1;
  }

  dl,
  dt {
    --flow-space: #{get-size("700")};
  }

  dd {
    --flow-space: #{get-size("300")};
  }
</style>

<section class="[ summary ] [ flow radius ] [ bg-primary color-light ]">
  <h3 class="color-tertiary-glare text-700">Summary</h3>
  <dl class="flow">
    <dt class="text-600 color-tertiary-glare">Balance</dt>
    <dd class="text-700 font-mono weight-bold">£{balance}</dd>
    <dt class="text-600 color-tertiary-glare">Total outgoings</dt>
    <dd class="text-700 font-mono weight-bold">-£{outgoings}</dd>
    <dt class="text-600 color-tertiary-glare">Total income</dt>
    <dd class="text-700 font-mono weight-bold">+£{income}</dd>
  </dl>
</section>
