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
  <div class="modal">🔋Discharge Means Creativity;는 💻🔋를 꽉꽉 채워서 모여
    방전될 때까지 놀다(?) 🏡에 가는 모임입니다. 모임 중간에 기분 좋으면 충전기
    👏🏼찬스👏🏼도 드려요. FTTO 멤버들이 방전을 연료로 창작을 달리는 여러분을 위해
    핸드드립 ☕️도 제공합니다.</div>
</div>
