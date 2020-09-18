<script>
  import { Router, Route, Link, link } from "svelte-routing";
  import Header from "./components/Header.svelte";
  import Footer from "./components/Footer.svelte";
</script>

<style>
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

</style>

<main>
  <Header />
  <Footer />
</main>
