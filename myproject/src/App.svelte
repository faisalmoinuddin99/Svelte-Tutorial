<script>
  let name = "naruto";
  let beltColor = "black";
  let first_name = "Jimmy";
  let last_name = "sharma";

  // Reactive Value
  $: full_name = `${first_name} ${last_name}`;

  // Reactive Statement
  $: console.log(beltColor);

  $: {
    console.log(beltColor);
    console.log(full_name);
  }

  let handleClick = () => {
    if (beltColor == "black") {
      beltColor = "yellow";
    } else {
      beltColor = "black";
    }
  };

  let handleInput = (e) => {
    beltColor = e.target.value;
  };
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>{full_name} - {beltColor} belt</p>

  <button on:click={handleClick}>update belt color</button>

  <!-- one-way data binding -->
  <input type="text" on:input={handleInput} value={beltColor} />

  <hr />

  <input type="text" bind:value={first_name} />
  <input type="text" bind:value={last_name} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
