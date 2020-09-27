<script>
  import FaFacebookSquare from "svelte-icons/fa/FaFacebookSquare.svelte";
  import FaInstagram from "svelte-icons/fa/FaInstagram.svelte";
</script>

<style lang="scss">
  .Artist {
    height: 130vh;
    background-image: url("https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/wallpaper-artist.jpg?alt=media&token=110247ae-72d9-462e-a25c-9a47ffd84481");
    background-size: cover;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    color: white;
  }
  .container-artist {
    width: 45vw;
  }
  .name {
    display: flex;
    justify-content: center;
    font-style: normal;
    font-weight: 600;
    font-size: 43px;
  }
  .name p {
    margin: 0;
    padding: 0;
    text-align: center;
    align-items: center;
  }
  .description {
    display: flex;
    justify-content: center;
  }
  .description p {
    font-size: 1.3em;
    text-align: center;
  }
  .name p span {
    font-size: 0.3em;
  }
  .avatar {
    display: flex;
    justify-content: center;
  }
  .redes {
    display: flex;
    justify-content: center;
  }
  .redes .icon {
    width: 2em;
    margin: 1em 1em 0 0;
    color: white;
  }
  .avatar img {
    border-radius: 100%;
  }
  #avatar-julia img {
    width: 150px;
    height: 150px;
  }
    #facebook:hover{
    color:#3b5998;
  }
  #instagram:hover{
    color:#e1306c;
  }
  @media screen and (max-width: 768px) {
  }
  @media screen and (max-width: 700px) {
    .Artist {
      flex-direction: column;
      background-image: none;
      color: white;
      margin-bottom: -2em;
      .container-artist {
        margin-bottom: 2em;
        padding: 1em;
        height: 110vh;
        width: 100vw;
        background-image: url("https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Fwallpaper-artist-min.jpg?alt=media&token=614a5901-1863-4dff-b24d-96630e06391b");
        background-size: cover;
        .description p {
          font-size: 1em;
          width: 60vw;
          text-align: center;
        }
      }
    }
  }
  @media screen and (max-width: 425px) {
    .Artist .container-artist .description p {
      font-size: 0.9em;
      width: 80vw;
    }
  }
</style>

<div class="Artist">
  <div class="container-artist">
    <div class="name">
      <div class="container-name">
        <p>Bodymood</p>
        <p><span>Omar</span></p>
      </div>
    </div>
    <div class="description">
      <p>
        Despues de diez años de arduo trabajo y ejercicio del oficio han pasado
        por nuestro estudio, un selecto numero de artistas que sen han
        convertido en referentes en cada uno de sus estilos en la escena
        nacional, siendo big brother una de las tiendas mas influyentes en el
        creciente panorama del tatuaje en Colombia, con un equipo siempre en
        renovación ofreciendo experiencia pasión y profesionalismo.
      </p>
    </div>
    <div class="avatar">
      <img
        src="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-19/s150x150/43282929_2137980146455650_9077043476037632000_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_ohc=E_TZCz9wUOsAX_FwTEZ&oh=d6bc7091e6b121fb0cb6a484d8205c02&oe=5F824CD8"
        alt="" />
    </div>
    <div class="redes">
      <a href="/"><div id="facebook" class="icon">
          <FaFacebookSquare />
        </div></a>
      <a href="/"><div id="instagram" class="icon">
          <FaInstagram />
        </div></a>
    </div>
  </div>
  <div class="container-artist">
    <div class="name">
      <div class="container-name">
        <p>Imelo</p>
        <p><span>Julianny Hernández </span></p>
      </div>
    </div>
    <div class="description">
      <p>
        Despues de diez años de arduo trabajo y ejercicio del oficio han pasado
        por nuestro estudio, un selecto numero de artistas que sen han
        convertido en referentes en cada uno de sus estilos en la escena
        nacional, siendo big brother una de las tiendas mas influyentes en el
        creciente panorama del tatuaje en Colombia, con un equipo siempre en
        renovación ofreciendo experiencia pasión y profesionalismo.
      </p>
    </div>
    <div class="avatar" id="avatar-julia">
      <img
        src="https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Fartis2-min.jpg?alt=media&token=bce7b807-6352-4250-b182-771701215125"
        alt="avatar2.png" />
    </div>
    <div class="redes">
      <a href="/"><div id="facebook" class="icon">
          <FaFacebookSquare />
        </div></a>
      <a href="/"><div id="instagram" class="icon">
          <FaInstagram />
        </div></a>
    </div>
  </div>
</div>