<script>
  import { fade } from "svelte-transitions";
  import "boxicons";
  const img = [
    "./images/img1.jpg",
    "./images/img2.jpg",
    "./images/img3.jpg",
    "./images/img4.jpg",
    "./images/img5.jpg",
    "./images/img6.jpg",
    "./images/img7.jpg",
  ];
  async function ShowImage() {
    setTimeout(() => {
      const images = document.querySelectorAll(".img");
      const containerImage = document.querySelector(".layer");
      const coverImage = document.querySelector(".img-cover");
      images.forEach((img) => {
        img.addEventListener("click", () => {
          addImage(img.getAttribute("src"));
        });
      });
      const addImage = (src) => {
        containerImage.classList.toggle("move");
        coverImage.classList.toggle("show");
        coverImage.src = src;
      };
      containerImage.addEventListener("click", () => {
        containerImage.classList.toggle("move");
        coverImage.classList.toggle("show");
      });
    }, 1);
  }

  ShowImage();
</script>

<style lang="scss">
  .Tatuados {
    margin-top: 16vh;
    .container-grid {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
      grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr;
      grid-template-areas: "img1 img2 img3 img3 img3" "img1 img2 img3 img3 img3" "img4 img4 img3 img3 img3" "img4 img4 img3 img3 img3" "img6 img6 img5 img5 img5" "img6 img6 img5 img5 img5";
      width: 100vw;
      height: 70vh;
      .img {
        object-fit: cover;
        width: 100%;
        height: 100%;
        filter: grayscale(50%);
      }

      :hover {
        cursor: pointer;
        filter: none;
      }

      .img1 {
        grid-area: img1;
      }

      .img2 {
        grid-area: img2;
      }

      .img3 {
        grid-area: img3;
      }

      .img4 {
        grid-area: img4;
      }

      .img5 {
        grid-area: img5;
      }

      .img6 {
        grid-area: img6;
      }
    }
  }
  .layer {
    position: absolute;
    width: 100vw;
    height: 100vh;
    background-color: rgba(12, 12, 12, 0.5);
    transform: translateX(-100%);
    transition: transform .5s ease-in;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    .container-img {
      position: relative;
      width: 100%;
      height: 85%;
      img {
        position: absolute;
        width: 100%;
        height: 100%;
        transform: scale(0.8);
        object-fit: cover;
      }
    }
    .icon {
      position: absolute;
      right: 0;
      top: 0;
      margin: 2em 3.5em;
    }
  }


  .layer.move {
    transform: translateX(0);
  }
</style>

<div class="Tatuados">
  <div class="container-grid">
    <img src={img[0]} alt="" class="img img1" />
    <img src={img[1]} alt="" class="img img2" />
    <img src={img[2]} alt="" class="img img3" />
    <img src={img[3]} alt="" class="img img4" />
    <img src={img[4]} alt="" class="img img5" />
    <img src={img[5]} alt="" class="img img6" />
    <div class="layer move" transition:fade>
      <div class="container-img">
        <img class="img-cover" src={img[5]} alt="" />
      </div>
      <box-icon class="icon" name="x-circle" color="#ffffff" />
    </div>
  </div>
</div>
