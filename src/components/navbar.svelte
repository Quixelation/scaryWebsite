<script>
  import { link } from "svelte-spa-router";
  import { location } from "svelte-spa-router";
  var time = "";
  var timeELem;
  import { onMount } from "svelte";

  onMount(async () => {
    startTime();
  });
  function startTime() {
    var today = new Date();
    var h = today.getHours();
    var m = today.getMinutes();
    var s = today.getSeconds();
    var d = today.getDate();
    var y = today.getFullYear();
    var mo = today.getMonth() + 1;

    m = checkTime(m);
    s = checkTime(s);
    d = checkTime(d);
    mo = checkTime(mo);

    timeELem.innerHTML =
      d +
      "." +
      mo +
      "." +
      y +
      " " +
      h +
      ":" +
      m +
      ":" +
      s +
      "&nbsp&nbsp&nbsp&nbsp";
    var t = setTimeout(startTime, 500);
  }
  function checkTime(i) {
    if (i < 10) {
      i = "0" + i;
    }
    return i;
  }
</script>

<nav class="mainPadding">
  <a href="#" class="navTitle">Clemens Greulich</a>
  <ul>
    <li>
      <a href="#"><span>Home</span></a>
    </li>
    <li><a href="#twitch"><span>Twitch</span></a></li>
    <li><a href="#youtube"><span>Youtube</span></a></li>
    <li><a use:link href="/instagram"><span>Instagram</span></a></li>
    <li><a use:link href="/impressum"><span>Impressum</span></a></li>
  </ul>
  <span class="time" bind:this={timeELem} />
</nav>

<style>
  nav {
    height: 50px;
    background-color: #222222a4;
    -webkit-backdrop-filter: blur(5px);
    backdrop-filter: blur(5px);
    display: flex;
    align-items: center;
    position: fixed;
    left: 0;
    top: 0;
    z-index: 9999;
    width: 100%;
  }
  .navTitle {
    font-weight: 600;
    color: white;
    font-size: 18px;
    text-decoration: none;
    transition: transform 0.175s ease;
  }
  .navTitle:hover {
    /* transform: scale(1.1); */
  }
  ul {
    list-style-type: none;
    display: flex;
    height: 100%;
    align-items: center;
  }
  ul > li {
    padding-left: 10px;
    padding-right: 10px;
    height: 100%;
  }

  ul > li > a {
    text-decoration: none;
    height: 100%;
    color: #9d9d9d;
    display: grid;
    place-items: center;
    cursor: pointer;
  }
  ul > li > a:hover {
    color: white;
  }
  .time {
    float: left;
  }
</style>
