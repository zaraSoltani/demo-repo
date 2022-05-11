<script>
  import Nav from "../components/Nav.svelte";
  import HamburgerMenu from "./HamburgerMenu.svelte";
</script>

<div class="navigation">
  <div class="content">
    <img src="spaceIcon.png" alt="icon" />
    <h2><b>Z</b>ara<b>E</b>xplains!</h2>
  </div>
  <div class="wrapper">
    <Nav />
    <HamburgerMenu />
  </div>
</div>

<style>
  .navigation {
    background: url("https://cff2.earth.com/uploads/2016/09/06113601/scandinavia_nighttime_1big_iss_nasa.jpg")
      no-repeat;
    background-size: cover;
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
  .content img {
    max-width: 50px;
    z-index: 10;
  } 
  .content {
    max-width: 300px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 2rem;
    padding-left: 4rem;
  }
  .content h2 {
    color: white;
    padding-left: 0.5rem;
    font-family: "Amatic SC", cursive;
    font-size: 30px;
    margin-bottom: 0px;
    letter-spacing: 3px;
  }
  b {
    font-size: 46px;
  }
  .wrapper {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    min-width: 55%;
  }
</style>
