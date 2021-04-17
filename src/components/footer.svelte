<script>
  import { link } from "svelte-spa-router";
</script>

<div class="footer mainPadding">
  <div>
    <img src="assets/scaryMikrowelleLogo.jpg" alt="scaryMikrowelle Logo" />
    <span>Clemens Greulich</span>
  </div>
  <div>
    <a href="/licenses.html">Lizenzen</a>
    <a use:link href="/impressum">Impressum</a>
  </div>
</div>

<style lang="scss">
  .footer {
    background-color: #333333;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: {
      top: 5px;
      bottom: 5px;
    }

    img {
      border-radius: 50%;
      height: 35px;
    }
    > div {
      display: flex;
      align-items: center;
      gap: 15px;
    }
    a {
      text-decoration: none;
      color: #eee;
      border-bottom: 2px dotted #eee;
      &:hover {
        border-bottom-style: solid;
      }
    }
  }
</style>
