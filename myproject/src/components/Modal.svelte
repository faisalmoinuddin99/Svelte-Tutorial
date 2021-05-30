<script>
  export let showModal;
  export let isPromo;
  export let message = "default";

  /*
  * Event Modifier: 
  1. once - make sure the event can only fire once (remove handler)
  2. preventDefault - prevent the default action (run e.preventDefault())
  3. self - only fires the event if the clicked element is the target
  */
</script>

{#if showModal === true}
  <!-- Event Forwarding -->
  <div class="backdrop" class:promo={isPromo} on:click|self>
    <div class="modal">
      <p>{message}</p>
    </div>
  </div>
{/if}

<style>
  .backdrop {
    width: 100%;
    height: 100%;
    position: fixed;
    background: rgba(0, 0, 0, 0.8);
  }

  .modal {
    padding: 10px;
    border-radius: 10px;
    max-width: 400px;
    margin: 10% auto;
    text-align: center;
    background: white;
  }
  .promo .modal {
    background-color: crimson;
    color: white;
  }
</style>
