<script>
  import Navbar from "./../components/navbar.svelte";
  import MainPage from "./../pages/main.svelte";
  import TwitchPage from "./../pages/twitch.svelte";
  import YoutubePage from "./../pages/youtube.svelte";
</script>

<Navbar />

<MainPage />
<div id="twitch">
  <svg
    class="marginTopSvg"
    style="vertical-align:top; ;"
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 1440 320"
  >
    <path
      fill="#512da8"
      fill-opacity="1"
      d="M0,192L48,197.3C96,203,192,213,288,229.3C384,245,480,267,576,250.7C672,235,768,181,864,181.3C960,181,1056,235,1152,234.7C1248,235,1344,181,1392,154.7L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
    />
  </svg>
  <TwitchPage />
</div>
<div id="youtube">
  <svg
    style="vertical-align:top"
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 1440 320"
    ><path
      fill="#512da8"
      fill-opacity="1"
      d="M0,160L48,160C96,160,192,160,288,138.7C384,117,480,75,576,64C672,53,768,75,864,90.7C960,107,1056,117,1152,122.7C1248,128,1344,128,1392,128L1440,128L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z"
    /></svg
  >
  <YoutubePage />
</div>
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />

<style lang="scss">
  .marginTopSvg {
    margin-top: -150px;
    @media screen and (max-width: 800px) {
      margin-top: 0px;
    }
  }
</style>
