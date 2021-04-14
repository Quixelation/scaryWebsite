<script>
  let host = location.hostname;
  var twitchIframe;
  import { onMount } from "svelte";
  onMount(async () => {
    if(CSS?.supports?.("aspect-ratio","16 / 9")){
    twitchIframe.style.height = "unset"
  }
  });
  
  
</script>

<div class=" pageHeight page mainPadding">
  <h2 class="twitchTitle mainTitle">Twitch</h2>
  <div class="pageContent widthWrapper">
    <iframe bind:this={twitchIframe}
      title="Twitch"
      src="https://player.twitch.tv/?channel=scaryMikrowelle&parent={host}"
      frameborder="0"
      allowfullscreen="true"
      scrolling="no"
    />
    <div>
      <a
        class="mainTextLink"
        href="https://twitch.clemensgreulich.de"
        target="_blank"
        ><span class="linkPrefix">twitch.tv/</span><span class="twitchName"
          >scaryMikrowelle</span
        ></a
      >
    </div>
  </div>
</div>

<style lang="scss">
  iframe {
    height: 378px;
    width: 620px;
    aspect-ratio: 16 / 9;
    @media screen and (max-width: 800px) {
      //smoll
      width: 100%;
    }
  }
  .page {
    .pageContent {
      display: grid;
      grid-template-columns: 1fr 1fr;
      @media screen and (max-width: 1300px) {
        //smoll

        display: flex;
        flex-direction: column-reverse;
        @at-root .twitchTitle {
          margin-bottom: 0 !important;
        }
      }
      place-items: center;
    }

    background-color: #512da8;
  }
  .mainTextLink {
    font-size: 2em;
    @media screen and (max-width: 800px) {
      //smoll
      font-size: 1em;
    }
    color: rgba(255, 255, 255, 0.75);
    text-decoration: none;
    padding: {
      top: 50px;
      bottom: 50px;
    }
    display: flex;
    flex-direction: column;

    .twitchName {
      color: #fff;
      font-size: 2em;
      transition: color 0.25s ease;
      opacity: 1;
      font-weight: 600;
      margin-top: -20px;
      @media screen and (max-width: 800px) {
        //smoll
        margin-top: -5px;
      }
    }
    &:hover > .twitchName {
      color: #a886f8;
    }
  }
</style>
