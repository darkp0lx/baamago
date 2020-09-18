<script>
  import FaInstagram from "svelte-icons/fa/FaInstagram.svelte";
  import FaFacebookSquare from "svelte-icons/fa/FaFacebookSquare.svelte";
  import FaWhatsappSquare from "svelte-icons/fa/FaWhatsappSquare.svelte";
</script>

<style lang="scss">
  .Footer {
    height: 30vh;
    background-image: url("https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/bg-footer.png?alt=media&token=adf29962-9e50-4d69-9e61-ec27361365b5");
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    .redes {
      display: flex;
      justify-content: center;
      margin: 1em 0 1em 0;
    }
    .icon {
      color: white;
      width: 5em;
      margin-right: 1.5em;
      height: 5em;
    }
  }

  @media screen and (max-width: 425px) {
    .Footer {
      .direccion h2{
        font-size: 1em;
      }
      .icon {
      width: 1.9em;
      height: 1.9em;
    }
    }
  }
</style>

<div class="Footer">
  <div class="container-Footer">
    <div class="span"><span>siguenos</span></div>
    <div class="redes">
      <a target="_black" href="https://www.instagram.com/llinpiy_tattoo/"><div
          class="icon">
          <FaInstagram />
        </div></a>
      <a
        target="_black"
        href="https://web.facebook.com/Baamago-Tattoo-107734911064066">
        <div class="icon">
          <FaFacebookSquare />
        </div>
      </a>
      <a
        target="_black"
        href="https://api.whatsapp.com/send?phone=51961679302&text=Hola%21%20Me%20interesa%20&source=&data=&app_absent=https://wa.me/51961679302?text=Hola!%20Me%20interesa%20"><div
          class="icon">
          <FaWhatsappSquare />
        </div>
      </a>
    </div>
    <div class="direccion">
      <h2>Jr jaquijahuana n°514/Izcuchaca-Anta</h2>
    </div>
  </div>
</div>
