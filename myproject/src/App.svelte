<script>
  import Modal from "./components/Modal.svelte";

  let showModal = false;

  let toggleModal = () => {
    showModal = !showModal;
  };
</script>

<main>
  <!-- <Modal message="Hey, I am a prop value" isPromo={true} /> -->
  <Modal message="I am another modal" {showModal} on:click={toggleModal} />
  <button on:click={toggleModal}> Show Modal</button>
  <h1>Hello world</h1>
</main>

<style>
</style>
