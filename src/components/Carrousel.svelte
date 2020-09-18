<script>
  import { fade } from "svelte/transition";
  const carouselPhotos = [
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/wallpaper.jpg?alt=media&token=a63ea5cb-f2a9-4dfe-ad11-f3a7371c66aa",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/wallpaper2.jpg?alt=media&token=63b26278-7bf4-49a9-890e-8a38119225ae",
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
