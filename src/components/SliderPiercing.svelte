<script>
  import { fade } from "svelte/transition";
  const carouselPhotos = [
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Fpiercing1-min.jpg?alt=media&token=8825bedf-8846-4137-b6f9-6572d68d3f9d",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/pircing%2Fp7.jpeg?alt=media&token=e3b9c029-f247-47ac-808a-454b821e93fb",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/pircing%2Fp6.jpeg?alt=media&token=85199934-1bf8-4a47-9ff7-3aa3aade3a9e",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/pircing%2Fp5.jpeg?alt=media&token=0ba3c0d2-b10a-414e-ae39-8bcbb04a0db3",
  ];

  let index = 0;
  setInterval(() => {
    before();
  }, 3000);
  const next = () => {
    index = (index + 1) % carouselPhotos.length;
  };
  const before = () => {
    if (index == 0) {
      index = carouselPhotos.length - 1;
    } else {
      index = (index - 1) % carouselPhotos.length;
    }
  };
</script>

<style lang="scss">
  .SliderPiercing {
    width: 100vw;
    height: 100vh;
  }
  .SliderPiercing h2 {
    text-align: center;
  }
  .container-img {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .container-img img {
    position: absolute;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    top: 10vh;
    text-align: center;
    width: 65vw;
    height: 65vh;
  }
  @media screen and(max-width:700px) {
  }
  @media screen and(max-width:425px) {
    .container-img {
      margin-top: -2em;
    }
  }
</style>

<div class="SliderPiercing">
  <div class="container-sliderPiercing">
    <h2>Piercing</h2>
    {#each [carouselPhotos[index]] as src (index)}
      <div class="container-img">
        <img transition:fade {src} alt="wallpaper.png" />
      </div>
    {/each}
  </div>
</div>
