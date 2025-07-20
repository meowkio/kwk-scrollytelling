<script>
  export let billItems = [];
</script>

<section>
  <h2>Hospital Bill</h2>
  <ul>
    {#each billItems as items}
      <li class={items.covered ? "covered" : "uncovered"}>
        {items.description} ---- ${items.amount}
      </li>
    {/each}
  </ul>
</section>

<style>
  ul {
    list-style: none;
    padding: 0;
  }

  li {
    font-size: 1.1rem;
    margin: 0.25rem 0;
  }

  .covered {
    text-decoration: line-through;
    color: #aaa;
  }

  .uncovered {
    font-weight: bold;
    color: #c0392b;
  }
</style>
