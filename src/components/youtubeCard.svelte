<script lang="ts">
  export let title: string;
  export let description: string;
  export let logoUrl: string;
  export let link: string;
</script>

<a href={link} class="ytCard" target="_blank">
  <img class="cardImg" alt="Youtube Kanal Logo" src={logoUrl} />
  <div class="cardContentContainer">
    <h3 class="ytChannelTitle">{title}</h3>
    <p class="ytChannelDescription">
      {description ? description : ""}
    </p>
  </div>
</a>

<style lang="scss">
  .ytCard {
    color: white;
    cursor: pointer;
    text-decoration: none;
    display: flex;
    flex-direction: column;
    align-items: center;
    .cardImg {
      z-index: 12;
      border-radius: 50%;
      margin: {
        left: auto;
        right: auto;
      }
      transform: translateY(40%);
      transition: transform 0.25s ease, box-shadow 0.25s ease;
      transform-origin: center;
    }
    .cardContentContainer {
      height: 100%;
      border-radius: 5px;
      background-color: #2b2b2b;
      padding: 15px;
      width: 100%;
      z-index: 9;
      transition: box-shadow 0.25s ease;
      .ytChannelTitle {
        font-size: 2em;
        text-align: center;
      }
      .ytChannelDescription {
        color: rgb(170, 170, 170);
      }
    }
    &:hover {
      .cardImg {
        z-index: 3003;
        transform: scale(1.1) translateY(30%);
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
      }
      .cardContentContainer {
        box-shadow: 0 19px 38px rgba(0, 0, 0, 0.3),
          0 15px 12px rgba(0, 0, 0, 0.22);
        z-index: 3000;
      }
    }
    @media screen and (max-width: 600px) {
      //smoll
      flex-direction: row;
      .cardImg {
        transform: none;
        margin-right: -25px;
      }
      .cardContentContainer {
        padding-left: 15px + 25px;
      }
      &:hover {
        .cardImg {
          transform: none;
        }
      }
    }
  }
</style>
