<script>
  import Modal from "./components/Modal.svelte";

  let showModal = false;

  let toggleModal = () => {
    showModal = !showModal;
  };
</script>

<main>
  <!-- <Modal message="Hey, I am a prop value" isPromo={true} /> -->
  <Modal {showModal} on:click={toggleModal}>
    <!-- <h4>Add a new person</h4> -->
    <form>
      <input type="text" placeholder="name" />
      <input type="text" placeholder="belt color" />
      <button>Add person</button>
    </form>
    <div slot="title">
      <h3>Add a new person</h3>
    </div>
  </Modal>
  <button on:click|once={toggleModal}> Show Modal</button>
  <h1>Hello world</h1>
</main>

<style>
  button {
    background-color: lightblue;
    color: black;
    font-size: 25px;
    margin: auto;
  }
</style>
