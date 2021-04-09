<script>
  import Navbar from "./../components/navbar.svelte";
</script>

<Navbar />
<div class="page">
  <table class="tg">
    <tbody>
      <tr>
        <td>Name</td>
        <td>Clemens Jonathan Greulich</td>
      </tr>
      <tr>
        <td>Kontakt</td>
        <td
          ><a href="tel:+4915123455552">+4915123455552</a><br /><a
            href="mailto:clemens@clemensgreulich.de"
            >clemens@clemensgreulich.de</a
          ></td
        >
      </tr>

      <tr>
        <td>Anschrift</td>
        <td
          ><address>
            Marderweg 7<br />07749<br />Jena<br />Deutschland
          </address></td
        >
      </tr>
    </tbody>
  </table>
</div>

<style lang="scss">
  .page {
    margin-top: 30px;
    display: grid;
    place-items: center;
  }
  tr > td {
    vertical-align: top;
    &:first-of-type {
      padding-right: 30px;
      font-weight: bold;
      text-align: right;
    }
    &:last-of-type {
      padding-bottom: 15px;
    }
  }
</style>
