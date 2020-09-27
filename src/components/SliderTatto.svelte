<script>
  import { fade } from "svelte/transition";
  const carouselPhotos = [
    "https://scontent.faqp4-1.fna.fbcdn.net/v/t1.0-9/118496189_596348691047973_4081341248955873775_o.jpg?_nc_cat=102&_nc_sid=a26aad&_nc_eui2=AeHcAANNAf7xyrAG2-r-nyKvdfjzcwGJ_at1-PNzAYn9q9aSB4fwUKHGgEllsVWOt_zoXR-NQ2J0Vq2fnPrp5yaO&_nc_ohc=V4xUA0EZ9GUAX9pQjqv&_nc_oc=AQm6CBo8-EFHdjNgsU-o4bMNwP2HvjRamenquxWM1MSvJZKOm5hpmHf2onRVis6s3xk&_nc_ht=scontent.faqp4-1.fna&oh=50617e24a908a84fa7917706f18a128d&oe=5F97643C",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto1-min.jpeg?alt=media&token=09ffd9db-e5d8-4af4-b1c4-cc9155a050fc",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto3.png?alt=media&token=75a6edf1-6fba-4e90-8035-ac440b48841c",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto6.png?alt=media&token=57397f3e-a005-4aef-b44c-e7e09bdcf9cf",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto7-min.jpg?alt=media&token=cdb98e71-3efe-461d-92e5-e771bdf66314",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto10.png?alt=media&token=d3048021-8d56-41e6-9bc5-1f3657d63315",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto12.png?alt=media&token=aabd8f97-6ba9-410d-b498-a8481ee6cf1c",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/seo-image%2Ftatto13.png?alt=media&token=3d7ebb5c-2907-45f0-9d33-c29aef0f5609"
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
  .SliderTatto {
    width: 100vw;
    height: 100vh;
    margin-top: 7vh;
  }
  .SliderTatto h2 {
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
    .SliderTatto {
      height: 100vh;
      width: 100%;
      margin-top: 55vh;
    }
  }
  @media screen and(max-width:425px){
    .container-img,img{
    margin-top: -2em;
    }
  }
</style>

<div class="SliderTatto">
  <div class="container-sliderTatto">
    <h2>Tattos</h2>
    {#each [carouselPhotos[index]] as src (index)}
      <div class="container-img">
        <img transition:fade {src} alt="wallpaper.png" />
      </div>
    {/each}
  </div>
</div>
