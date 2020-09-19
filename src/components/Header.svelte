<script>
  import { Router, Route, Link, link } from "svelte-routing";
  import Home from "../Home.svelte";
  import Studio from "../Studio.svelte";
  import Tattos from "../Tattos.svelte";

  import IoIosMenu from "svelte-icons/io/IoIosMenu.svelte";
  import FaWhatsapp from "svelte-icons/fa/FaWhatsapp.svelte";
  import FaInstagram from "svelte-icons/fa/FaInstagram.svelte";
  import FaFacebookSquare from "svelte-icons/fa/FaFacebookSquare.svelte";

  function active_modal() {
    var element = document.getElementById("active");
    if (element.classList.length == 0) {
      element.classList.add("modal-menu");
    } else {
      element.classList.toggle("modal-menu");
    }
  }
</script>

<style lang="scss">
  .Header nav {
    width: 30vw;
    display: flex;
    justify-content: space-between;
    .icon {
      width: 2em;
      height: 2em;
    }
    .redes {
      display: flex;
    }
    a {
      color: black;
    }
  }

  .Header-container {
    display: flex;
    position: fixed;
    top: 0;
    justify-content: space-evenly;
    z-index: 2;
    width: 100vw;
    align-items: center;
    background-color: #fff;
    -webkit-box-shadow: 10px 2px 5px 0px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 10px 2px 5px 0px rgba(0, 0, 0, 0.75);
    box-shadow: 10px 2px 5px 0px rgba(0, 0, 0, 0.75);
    .menu .icon {
      width: 2em;
      height: 2em;
      display: none;
    }
  }

  @media screen and (max-width: 700px) {
    .Header .active {
      display: none;
    }
    .Header .modal-menu {
      display: flex;
      position: fixed;
      top: 0;
      z-index: 1;
      right: 0;
      margin-top: 18vh;
      justify-content: center;
      width: 100%;
      height: 51vh;
      align-items: center;
      background: white;
      -webkit-box-shadow: -1px 14px 16px -12px rgba(0, 0, 0, 0.75);
      -moz-box-shadow: -1px 14px 16px -12px rgba(0, 0, 0, 0.75);
      box-shadow: -1px 14px 16px -12px rgba(0, 0, 0, 0.75);
      nav {
        display: block;
        justify-content: center;
        ul li {
          list-style: none;
          margin-bottom: 0.5em;
        }
        a {
          color: black;
          font-size: 2em;
        }
      }
      .redes {
        justify-content: center;
      }
    }
    .Header-container {
      justify-content: space-between;
      img {
        margin-left: 5vw;
      }
      .menu {
        margin-right: 5vw;
        .icon {
          display: block;
        }
      }
    }
  }
</style>

<div class="Header">
  <Router>
    <div class="Header-container">
      <nav class="active">
        <a href="/" use:link>Home</a>
        <a href="/Studio" use:link>Studio</a>
      </nav>
      <img
        src="https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/LOGO%20TATTO.png?alt=media&token=3b5a48d2-faec-4dfb-a34e-a0795bef8541"
        alt="logo.png" />
      <nav class="active">
        <a href="/Tattos" use:link>Tattos</a>
        <div class="redes">
          <a
            target="_black"
            href="https://web.facebook.com/Baamago-Tattoo-107734911064066">
            <div class="icon">
              <FaFacebookSquare />
            </div>
          </a>
          <a
            target="_black"
            href="https://www.instagram.com/llinpiy_tattoo/"><div class="icon">
              <FaInstagram />
            </div>
          </a>
          <a
            target="_black"
            href="https://api.whatsapp.com/send?phone=51961679302&text=Hola%21%20Me%20interesa%20&source=&data=&app_absent=https://wa.me/51961679302?text=Hola!%20Me%20interesa%20"><div
              class="icon">
              <FaWhatsapp />
            </div>
          </a>
        </div>
      </nav>
      <div class="menu">
        <div id="menu" class="icon" on:click={active_modal}>
          <IoIosMenu />
        </div>
      </div>
    </div>
    <div class="modal-menu" id="active">
      <nav>
        <ul>
          <li><a href="/" use:link>Home</a></li>
          <li><a href="/Studio" use:link>Studio</a></li>
          <li><a href="/Tattos" use:link>Tattos</a></li>
        </ul>
        <div class="redes">
          <a
            target="_black"
            href="https://web.facebook.com/Baamago-Tattoo-107734911064066">
            <div class="icon">
              <FaFacebookSquare />
            </div>
          </a>
          <a
            target="_black"
            href="https://www.instagram.com/llinpiy_tattoo/"><div class="icon">
              <FaInstagram />
            </div>
          </a>
          <a
            target="_black"
            href="https://api.whatsapp.com/send?phone=51961679302&text=Hola%21%20Me%20interesa%20&source=&data=&app_absent=https://wa.me/51961679302?text=Hola!%20Me%20interesa%20"><div
              class="icon">
              <FaWhatsapp />
            </div>
          </a>
        </div>
      </nav>
    </div>
    <div>
      <Route path="/" component={Home} />
      <Route path="/Studio" component={Studio} />
      <Route path="/Tattos" component={Tattos} />
    </div>
  </Router>
</div>
