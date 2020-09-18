<script>
  import { fade } from "svelte/transition";
  const carouselPhotos = [
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/tatto2.jpg?alt=media&token=bf337bcd-7bda-4228-a291-65abf243df3f",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/tatto1.jpg?alt=media&token=fd74ec00-582c-400e-ae47-3ce70753cefd",
    "https://scontent.faqp4-2.fna.fbcdn.net/v/t1.0-9/118863937_600961797253329_87000584461393436_o.jpg?_nc_cat=100&_nc_sid=a26aad&_nc_eui2=AeFBLnLd51oL4aFR6B-3R9VyS4YcsUH-W1ZLhhyxQf5bVuuLem1WgoMOx4-F5d33kN7AW5hL6Fhj2uyg1SP_ojCR&_nc_ohc=IrrTnexntaUAX-weBFE&_nc_ht=scontent.faqp4-2.fna&oh=d397d3b13cbb623a0e0d53533f85b192&oe=5F7CEAB0",
    "https://scontent.faqp4-1.fna.fbcdn.net/v/t1.0-9/118496189_596348691047973_4081341248955873775_o.jpg?_nc_cat=102&_nc_sid=a26aad&_nc_eui2=AeHcAANNAf7xyrAG2-r-nyKvdfjzcwGJ_at1-PNzAYn9q9aSB4fwUKHGgEllsVWOt_zoXR-NQ2J0Vq2fnPrp5yaO&_nc_ohc=Vyk9xlkt4IYAX9y2d6_&_nc_oc=AQlLSROBNr74MxFm7LAYmtX98XGjQE1G9Qaeq3WSuMRYjuCXqJ-K8fNYRMyAM6fWfv0&_nc_ht=scontent.faqp4-1.fna&oh=00e1ec494af08a35fddcf841abc3a643&oe=5F7FA93C",
    "https://scontent.faqp4-2.fna.fbcdn.net/v/t1.0-9/118387241_596223034393872_3545899982573068492_o.jpg?_nc_cat=106&_nc_sid=a26aad&_nc_eui2=AeGO_rdgLOeiTW5wPQkMXzxUgA6PQwWoB3OADo9DBagHcx7bIrUUcmhLajrumjIvwmNMIVkYagMa6pZkKw-9YpJD&_nc_ohc=5R8dFNiDIIIAX8K97jW&_nc_ht=scontent.faqp4-2.fna&oh=8bd592f2155624f3c71ff02d2ad1a1d7&oe=5F802D26",
    "https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/tatto7.png?alt=media&token=3446534f-cbd5-44ec-843e-a00605d3b827",
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
