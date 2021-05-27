<script>
  let peope = [
    { id: 1, name: "Naruto", age: 20, beltcolor: "black" },
    { id: 2, name: "Saske", age: 21, beltcolor: "orange" },
    { id: 3, name: "Sakura", age: 20, beltcolor: "pink" },
  ];
</script>

<main>
  <table class="table">
    <thead>
      <tr>
        <th scope="col">ID</th>
        <th scope="col">NAME</th>
        <th scope="col">AGE</th>
        <th scope="col">BELT-COLOR</th>
      </tr>
    </thead>
    <tbody>
      {#each peope as ninja (ninja.id)}
        <tr>
          <th scope="row">{ninja.id}</th>
          <td>{ninja.name}</td>
          <td>{ninja.age}</td>
          <td>{ninja.beltcolor}</td>
        </tr>
      {:else}
        <p>There are no ninja to show...</p>
      {/each}
    </tbody>
  </table>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
