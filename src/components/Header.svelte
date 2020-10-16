<script>
  import { Router, Route, Link, link } from "svelte-routing";
  import GiHamburgerMenu from "svelte-icons/gi/GiHamburgerMenu.svelte";
  import Home from "../Home.svelte";
  import Studio from "../Studio.svelte";
  import Tattos from "../Tattos.svelte";
  import FaFacebookSquare from "svelte-icons/fa/FaFacebookSquare.svelte";
  import FaInstagram from "svelte-icons/fa/FaInstagram.svelte";
  import FaWhatsappSquare from "svelte-icons/fa/FaWhatsappSquare.svelte";
  import Tatuados from "../Tatuados.svelte"

</script>

<style lang="scss">
  .Header {
    width: 100vw;
    background-color: white;
    top: 0;
    left: 0;
    display: flex;
    position: fixed;
    justify-content: space-evenly;
    align-items: center;
    z-index: 100;
    -webkit-box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.75);
    box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.75);
    .icon {
      color: black;
    }
    #btn-menu {
      display: none;
    }
    label {
      display: none;
      width: 60px;
      padding: 10px;
      color: black;
      font-size: 30px;
      transition: all 500ms ease;
    }
    nav {
      width: 70vw;
    }
    nav ul {
      margin: 0;
      list-style: none;
      padding: 0;
      display: flex;
      justify-content: space-evenly;
      li a {
        text-decoration: none;
        color: black;
        display: block;
        padding: 15px 20px;
        transition: all 500ms ease;
        text-align: center;
      }
      :hover {
        background-color: rgba(255, 255, 255, 0.3);
      }
    }
  }
  .icon {
    width: 2em;
  }
  #whatsapp:hover{
    color:#25d366;
  }
  #facebook:hover{
    color:#3b5998;
  }
  #instagram:hover{
    color:#e1306c;
  }
  @media screen and (max-width: 768px) {
    .Header {
      justify-content: space-between;
      padding: 0 1em 0 1em;
      position: fixed;
    }
    .Header label {
      display: block;
    }
    .Header nav {
      position: absolute;
      background: white;
      width: 100%;
      margin-top: -100%;
      left: 0%;
      transition: all 500ms ease;
      z-index: 1;
      ul {
        flex-direction: column;
        border-top: 1px solid #fffa;
      }
    }
    #btn-menu {
      cursor: pointer;
    }
    #btn-menu:checked ~ nav {
      margin: 0;
      margin-top: 100px;
      left: 0%;
    }
  }
</style>

<Router>
  <div class="Header">
    <div class="logo">
      <img
        src="https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/LOGO%20TATTO.png?alt=media&token=3b5a48d2-faec-4dfb-a34e-a0795bef8541"
        alt="" />
    </div>
    <div class="nav">
      <input type="checkbox" id="btn-menu" />
      <label for="btn-menu" class="icon-menu"><div class="icon">
          <GiHamburgerMenu />
        </div></label>
      <nav>
        <ul>
          <li><a href="/" use:link>Home</a></li>
          <li><a href="/Studio" use:link>Studio</a></li>
          <li><a href="/Tatuados" use:link>Tattos</a></li>
          <li style="display:flex; justify-content:center">
            <a target="_black" href="https://web.facebook.com/Baamago-Tattoo-107734911064066"><div id="facebook" class="icon">
                <FaFacebookSquare />
              </div></a>
            <a target="_black" href="https://www.instagram.com/llinpiy_tattoo/"><div id="instagram" class="icon">
                <FaInstagram />
              </div></a>
            <a target="_black" href="https://api.whatsapp.com/send?phone=51961679302&text=Hola%21%20Me%20interesa%20&source=&data=&app_absent=https://wa.me/51961679302?text=Hola!%20Me%20interesa%20"><div id="whatsapp" class="icon">
                <FaWhatsappSquare />
              </div></a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
  <div>
    <Route path="/" component={Home} />
    <Route path="/Studio" component={Studio} />
    <Route path="/Tatuados" component={Tatuados} />
  </div>
</Router>
