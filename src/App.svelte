<script>
  import Modal from "./Modal.svelte";
  import Nav from "./Nav.svelte";

  let isModalOpened = false;

  const handleClickAbout = () => {
    openModal();
  };

  const handleCloseAboutModal = () => {
    closeModal();
  };

  function closeModal() {
    isModalOpened = false;
  }

  function openModal() {
    isModalOpened = true;
  }
</script>

<style>
  .main-image {
    width: 100%;
    height: 100%;
    background-image: url("images/discharge.jpg");
    background-position: center;
    background-size: contain;
  }

  .information {
    position: absolute;
    right: 50px;
    bottom: 50px;
    background-color: rgba(0, 0, 0, 0.4);
    padding: 10px;
  }

  h1 {
    text-align: right;
  }

  .date,
  .location {
    width: 100%;
    text-align: right;
  }
</style>

<Nav onClickAbout={handleClickAbout} />
{#if isModalOpened}
  <Modal onCloseModal={handleCloseAboutModal} />
{/if}
<div class="main-image" />
<div class="information">
  <h1>Discharge Means Creativity;</h1>
  <p class="date">2019년 06월 01일 | 방전이 창작이 될 때까지</p>
  <p class="location">
    <a href="https://place.map.kakao.com/1244159721" title="카카오맵: 닷페이스">닷페이스
      사무실</a>
  </p>
</div>
