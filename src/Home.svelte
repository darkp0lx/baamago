<script>
  import Carrousel from "./components/Carrousel.svelte";
  import InfoPage from "./components/InfoPage.svelte";
  import Artist from "./components/Artist.svelte";
  import SliderTatto from "./components/SliderTatto.svelte";
  import SliderPiercing from "./components/SliderPiercing.svelte";

  import Icon from "fa-svelte";
  import { faAd } from "@fortawesome/free-solid-svg-icons/faAd";

  let icon = faAd;
</script>
<style>
  main{
    margin-top: 13vh;
  }
</style>
<main>
  <Carrousel />
  <InfoPage />
  <Artist />
  <SliderTatto />
  <SliderPiercing />
</main>
