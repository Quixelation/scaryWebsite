<script lang="ts">
  import YoutubeCard from "./../components/youtubeCard.svelte";
</script>

<h2 class="mainTitle">YouTube</h2>
<div class="page mainPadding widthWrapper">
  <YoutubeCard
    title="scaryBestOf"
    description=" Hier gibt es Twitch-Highlights von scaryMikrowelle auf einem anderen Level
      zu sehen."
    logoUrl="assets/scaryBestOfLogo.jpg"
    link="https://youtube.clemensgreulich.de/"
  />
  <YoutubeCard
    title="scaryMikrowelle"
    logoUrl="assets/scaryMikrowelleLogo.jpg"
    link="https://www.youtube.com/channel/UCi5MOTDDA11mmVmuKHS1JpQ/"
  />
</div>

<style lang="scss">
  .page {
    display: grid;
    grid-template-columns: 1fr 1fr;

    @media screen and (max-width: 768px) {
      //smoll
      display: flex;
      flex-direction: column;
    }
    gap: 15px;
  }
</style>
