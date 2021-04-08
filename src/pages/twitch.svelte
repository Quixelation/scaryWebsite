<div class=" pageHeight page mainPadding">
  <h2 class="mainTitle">Twitch</h2>
  <div class="pageContent widthWrapper">
    <iframe
      title="Twitch"
      src="https://player.twitch.tv/?channel=scaryMikrowelle&parent=localhost"
      frameborder="0"
      allowfullscreen="true"
      scrolling="no"
      height="378"
      width="620"
    />
    <div>
      <a
        class="mainTextLink"
        href="https://www.twitch.tv/scaryMikrowelle/"
        target="_blank"
        ><span class="linkPrefix">twitch.tv/</span><span class="twitchName"
          >scaryMikrowelle</span
        ></a
      >
    </div>
  </div>
</div>

<style lang="scss">
  .page {
    .pageContent {
      display: grid;
      grid-template-columns: 1fr 1fr;
      place-items: center;
    }

    background-color: #512da8;
  }
  .mainTextLink {
    font-size: 2em;
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
    }
    &:hover > .twitchName {
      color: #a886f8;
    }
  }
</style>
