<style lang="scss">
  @import "../scss/helpers";
  .table-group {
    border: 1px solid get-color("grey");
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
  }

  h3 {
    --flow-space: #{get-size("600")};
  }

  table {
    --flow-space: 0.2rem;

    width: 100%;
    min-width: 30rem;
  }

  td,
  h3 {
    padding: 0.5rem 1rem;
  }

  tr:first-child {
    border-top: 1px solid get-color("grey");
  }

  tr:nth-child(odd) td {
    background: get-color("light-shade");
  }

  td:nth-child(3) {
    text-align: right;
  }
</style>

<section
  class="[ table-group ] [ flow radius ]"
  aria-labelledby="transaction-label">
  <h3 class="color-secondary-shade text-400 weight-medium">14th July 2020</h3>
  <table>
    <thead class="visually-hidden">
      <tr>
        <th>Description</th>
        <th>Category</th>
        <th>Amount</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td data-type="expense">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-tertiary color-light ]">
            Expenses
          </span>
        </td>
        <td>-£123.40</td>
      </tr>
      <tr>
        <td data-type="expense">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-quaternary color-light ]">
            Bills
          </span>
        </td>
        <td>-£70.40</td>
      </tr>
      <tr>
        <td data-type="bill">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-quaternary color-light ]">
            Bills
          </span>
        </td>
        <td>-£333.33</td>
      </tr>
    </tbody>
  </table>
  <h3 class="color-secondary-shade text-400 weight-medium">13th July 2020</h3>
  <table>
    <thead class="visually-hidden">
      <tr>
        <th>Description</th>
        <th>Category</th>
        <th>Amount</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td data-type="expense">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-tertiary color-light ]">
            Expenses
          </span>
        </td>
        <td>-£123.40</td>
      </tr>
      <tr>
        <td data-type="expense">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-quaternary color-light ]">
            Bills
          </span>
        </td>
        <td>-£70.40</td>
      </tr>
      <tr>
        <td data-type="bill">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-quaternary color-light ]">
            Bills
          </span>
        </td>
        <td>-£333.33</td>
      </tr>
    </tbody>
  </table>
  <h3 class="color-secondary-shade text-400 weight-medium">12th July 2020</h3>
  <table>
    <thead class="visually-hidden">
      <tr>
        <th>Description</th>
        <th>Category</th>
        <th>Amount</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td data-type="expense">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-tertiary color-light ]">
            Expenses
          </span>
        </td>
        <td>-£123.40</td>
      </tr>
      <tr>
        <td data-type="expense">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-quaternary color-light ]">
            Bills
          </span>
        </td>
        <td>-£70.40</td>
      </tr>
      <tr>
        <td data-type="bill">Lorem ipsum dolor sit amet</td>
        <td>
          <span class="[ pill ] [ radius bg-quaternary color-light ]">
            Bills
          </span>
        </td>
        <td>-£333.33</td>
      </tr>
    </tbody>
  </table>
</section>
