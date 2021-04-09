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
  <div class="routesContainer">
    <Router {routes} />
  </div>
  <div class="footerContainer">
    <Footer />
  </div>
</main>

<style lang="scss">
  :global(*) {
    box-sizing: border-box;
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
    scrollbar-width: thin;
    scrollbar-color: #2b2b2b #121212;
    &::-webkit-scrollbar-thumb {
      background-color: #2b2b2b;
      border-radius: 6px;
      border: 3px solid var(--scrollbarBG);
    }
    &::-webkit-scrollbar-track {
      background: #121212;
    }
    &::-webkit-scrollbar {
      width: 11px;
    }
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
    height: 100%;
    display: flex;
    flex-direction: column;
    .routesContainer {
      flex-grow: 1;
    }
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
