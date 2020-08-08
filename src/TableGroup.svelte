<script>
  export let transactions = [
    {
      date: "2020-07-15",
      description: "Lorem ipsum dolor sit amet",
      type: "expense",
      amount: -123.4,
    },
    {
      date: "2020-07-15",
      description: "Lorem ipsum dolor sit amet",
      type: "bill",
      amount: -70.4,
    },
    {
      date: "2020-07-15",
      description: "Lorem ipsum dolor sit amet",
      type: "bill",
      amount: -333.33,
    },
    {
      date: "2020-07-15",
      description: "Lorem ipsum dolor sit amet",
      type: "other",
      amount: -333.33,
    },
    {
      date: "2020-07-14",
      description: "Lorem ipsum dolor sit amet",
      type: "expense",
      amount: -123.4,
    },
    {
      date: "2020-07-14",
      description: "Lorem ipsum dolor sit amet",
      type: "bill",
      amount: -70.4,
    },
    {
      date: "2020-07-14",
      description: "Lorem ipsum dolor sit amet",
      type: "bill",
      amount: -333.33,
    },
    {
      date: "2020-07-13",
      description: "Lorem ipsum dolor sit amet",
      type: "expense",
      amount: -123.4,
    },
    {
      date: "2020-07-13",
      description: "Lorem ipsum dolor sit amet",
      type: "bill",
      amount: -70.4,
    },
    {
      date: "2020-07-13",
      description: "Lorem ipsum dolor sit amet",
      type: "bill",
      amount: -333.33,
    },
  ];

  const groupedTransactions = transactions.reduce((map, current) => {
    if (current.date in map) {
      map[current.date].push(current);
    } else {
      map[current.date] = [current];
    }
    return map;
  }, {});

  const transactionCategoryMap = {
    expense: "expenses",
    bill: "bills",
  };

  function getTransactionCategory(type) {
    const category = transactionCategoryMap[type];
    return category ? category : type;
  }

  function formatDateString(dateString) {
    const date = new Date(dateString);
    const options = { year: "numeric", month: "long", day: "numeric" };
    return date.toLocaleDateString(undefined, options);
  }

  function formatCurrency(number) {
    return new Intl.NumberFormat("en-GB", {
      style: "currency",
      currency: "GBP",
    }).format(number);
  }
</script>

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

  tr .pill {
    background: get-color("grey");
  }

  tr[data-type="expense"] .pill {
    background: get-color("tertiary");
  }

  tr[data-type="bill"] .pill {
    background: get-color("quaternary");
  }

  .pill {
    display: inline-block;
    padding: 0.3rem 0.35rem;
    font-size: get-size("400");
    text-decoration: none;
    line-height: 1;
    white-space: nowrap;
    text-align: center;

    // Capitalize only in english
    :global([lang*="en"]) & {
      text-transform: capitalize;
    }
  }
</style>

<section
  class="[ table-group ] [ flow radius ]"
  aria-labelledby="transaction-label">
  {#each Object.keys(groupedTransactions) as date}
    <h3 class="color-secondary-shade text-400 weight-medium">
      {formatDateString(date)}
    </h3>
    <table>
      <thead class="visually-hidden">
        <tr>
          <th>Description</th>
          <th>Category</th>
          <th>Amount</th>
        </tr>
      </thead>
      <tbody>
        {#each groupedTransactions[date] as transaction}
          <tr data-type={transaction.type}>
            <td>{transaction.description}</td>
            <td>
              <span class="[ pill ] [ radius color-light ]">
                {getTransactionCategory(transaction.type)}
              </span>
            </td>
            <td>{formatCurrency(transaction.amount)}</td>
          </tr>
        {/each}
      </tbody>
    </table>
  {/each}
</section>
