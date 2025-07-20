<script>
  import HospitalBill from "./lib/HospitalBill.svelte";
  import billData from "./data/hospital-bill.json";

  const bills = /** @type {any[]} */ (billData); //billData was being treated as unknown and not an array.. so this helped!

  console.log("App is loaded!");
  let msg = "Hello, Chloe!";
</script>

<main>
  <h1>{msg}</h1>
</main>

<style>
  .bill-container {
    margin: 2rem 0;
    padding: 1rem;
    border: 1px solid #ddd;
    border-radius: 0.5rem;
    background: #f9f9f9;
  }

  h2 {
    margin-bottom: 0.5rem;
    color: #333;
  }

  main {
    padding: 2rem;
    font-family: "Courier New", Courier, monospace;
    background-color: #e2e2e2e4;
  }
</style>
