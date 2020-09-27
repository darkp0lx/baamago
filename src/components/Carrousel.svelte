<script>
  import { fade } from "svelte/transition";
  const carouselPhotos = [
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Fwallpaper-new.jpg?alt=media&token=5656698b-6afd-4bec-af82-00e0a3c5d552",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Fwallpaper2-min.jpg?alt=media&token=20733e25-7d68-4902-b85b-873683d4d07c",
  ];

  let index = 0;
  setInterval(() => {
    before();
  }, 6000);
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

<style>
  .container-img {
    display: flex;
    justify-content: center;
    position: relative;
  }
  .container-img img {
    width: 60vw;
    height: 50vh;
    position: absolute;
  }
</style>

<div class="Carrousel">
  {#each [carouselPhotos[index]] as src (index)}
    <div class="container-img">
      <img transition:fade {src} alt="wallpaper.png" />
    </div>
  {/each}
</div>
