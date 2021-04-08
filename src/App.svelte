<script>
  import Router from "svelte-spa-router";

  import IndexPage from "./pages/index.svelte";
  import ImpressumPage from "./pages/impressum.svelte";
  import NotFoundPage from "./pages/404.svelte";
  import Footer from "./components/footer.svelte";
  const routes = {
    "/": IndexPage,
    "/impressum": ImpressumPage,
    "*": NotFoundPage,
  };
</script>

<main>
  <Router {routes} />
</main>
<Footer />

<style lang="scss">
  :global(*) {
    box-sizing: border-box;
  }
  :global(:root) {
    //font-size: 0.8em;
  }
  :global(.mainTitle) {
    font-family: "Lobster", cursive;
    text-align: center;
    font-size: 3em;
    font-weight: 400;
    margin-top: 0;
    text-decoration: underline;
  }
  :global(.widthWrapper) {
    max-width: 100%;
    margin-left: auto;
    margin-right: auto;
    width: 1250px;
    padding-left: 24px;
    padding-right: 24px;
  }
  :global(body) {
    margin: 0;
    padding: 0;
    background-color: #121212;
    color: #eee;
  }
  :global(html) {
    scroll-behavior: smooth;
  }
  :global(.mainMargin) {
    margin-right: 10px;
    margin-left: 10px;
  }
  :global(.mainPadding) {
    padding-right: 10px;
    padding-left: 10px;
  }
  main {
    margin-bottom: 30px;
  }
  @media screen and (min-width: 640px) {
    :global(.mainMargin) {
      margin-right: 64px;
      margin-left: 64px;
    }
    :global(.mainPadding) {
      padding-right: 64px;
      padding-left: 64px;
    }
  }
  :global(.pageHeight) {
    min-height: 60vh;
    @media screen and (max-width: 600px) {
      min-height: unset;
    }
  }
</style>
