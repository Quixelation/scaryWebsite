<div class="mainsection page mainPadding pageHeight">
  <div class="main_portrait_container">
    <div class="main_portrait">
      <img alt="Clemens Bild" src="assets/clemens_portrait.jpg" />
    </div>
    <img
      class="miniImg"
      alt="scary Bild"
      src="assets/scaryMikrowelleLogo.jpg"
    />
  </div>
  <div class="bigTextInfoContainer">
    <h1 class="title">Clemens Greulich</h1>
    <h3 class="subtitle">ScaryMikrowelle</h3>
  </div>
</div>

<style lang="scss">
  .page {
    &.mainsection {
      display: grid;
      grid-template-columns: 1fr 1fr;
      @media screen and (max-width: 600px) {
        //smoll
        margin-top: 100px;
        display: flex;
        flex-direction: column;
      }
      align-items: center;
      gap: 100px;
    }
    .main_portrait_container {
      justify-self: end;
      display: flex;
      justify-content: flex-end;
      flex-direction: column;

      position: relative;
      .main_portrait {
        width: 200px;
        height: 200px;
        overflow: hidden;
        border-radius: 25px;
        margin: auto;
        img {
          width: 100%;
          margin-top: -8px;
        }
      }
      .miniImg {
        position: absolute;
        border-radius: 50%;
        bottom: 0;
        right: 0;
        margin-left: auto;
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
        transform: translateY(50%) translateX(50%);
        width: 75px;
      }
    }

    .bigTextInfoContainer {
      .title {
        margin-bottom: 0px;
      }
      .subtitle {
        text-transform: uppercase;
        font-weight: bold;
        color: rgb(175, 175, 175);
        margin-top: 5px;
      }
    }
  }
</style>
