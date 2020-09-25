<script>
  import Carrousel from "./components/Carrousel.svelte";
  import InfoPage from "./components/InfoPage.svelte";
  import Artist from "./components/Artist.svelte";
  import SliderTatto from "./components/SliderTatto.svelte";
  import SliderPiercing from "./components/SliderPiercing.svelte";
  import { fly ,fade} from 'svelte/transition';

</script>
<style>
  main{
    margin-top: 13vh;
  }
</style>
<main in:fly="{{ y: 200, duration: 1500 }}" out:fade>
  <Carrousel />
  <InfoPage />
  <Artist />
  <SliderTatto />
  <SliderPiercing />
</main>
