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
    max-width: 80%;
    right: 2vw;
    bottom: 2vw;
    background-color: rgba(0, 0, 0, 0.4);
    padding: 10px;
  }

  h1,
  h3 {
    margin: 0;
    text-align: right;
  }

  h3 {
    margin-bottom: 10px;
  }

  p.description {
    text-align: right;
  }

  .date,
  .location {
    width: 100%;
    text-align: right;
  }

  @media only screen and (max-width: 640px) {
    h1 {
      font-size: 23px;
    }

    h3 {
      font-size: 18px;
    }
  }
</style>

<Nav onClickAbout={handleClickAbout} />
{#if isModalOpened}
  <Modal onCloseModal={handleCloseAboutModal} />
{/if}
<div class="main-image" />
<div class="information">
  <h1>Discharge Means Creativity;</h1>
  <h3>방전이 창작이 될 때까지</h3>

  <p class="date">2019년 06월 01일 | 오후 2시 ~ 🔋0% 🗓</p>
  <p class="location">
    <a href="https://place.map.kakao.com/1244159721" title="카카오맵: 닷페이스">닷페이스
      사무실</a>
    🗺
  </p>
</div>
