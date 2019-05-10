<script>
  export let onClickAbout;
</script>

<style>
  nav {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    height: 10px;
  }

  ul {
    display: flex;
    flex-direction: row;
    justify-content: end;
    padding: 0px 40px;
  }

  li {
    list-style: none;
    padding: 0px 10px;
    cursor: pointer;
  }
</style>

<nav>
  <ul>
    <li on:click={onClickAbout}>About?</li>
    <li>신청하기</li>
  </ul>
</nav>
