<script>
  let people = [
    { id: 1, name: "Naruto", age: 20, beltcolor: "black" },
    { id: 2, name: "Saske", age: 21, beltcolor: "orange" },
    { id: 3, name: "Sakura", age: 20, beltcolor: "pink" },
  ];
  const handleClick = (id) => {
    people = people.filter((ninja) => ninja.id != id);
  };
</script>

<main>
  <!-- svelte-ignore missing-declaration -->
  <Modal message="Hey, I am a prop value" isPromo={true} />
  <h4>Hello faisal</h4>
</main>

<style>
</style>
