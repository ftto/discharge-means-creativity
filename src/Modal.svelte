<script>
  export let onCloseModal;

  function clickDialog(e) {
    if (e.target !== this) {
      return;
    }

    onCloseModal();
  }
</script>

<style>
  .modal-dialog {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-content: center;
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 1000;
    background-color: rgba(0, 0, 0, 0.2);
    padding: 50px 50px;
  }

  .modal {
    background-color: white;
    width: 100%;
    max-width: 300px;
  }
</style>

<div class="modal-dialog" on:click={clickDialog}>
  <div class="modal">modal-body</div>
</div>
