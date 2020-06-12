<script>
  import Form from "../Components/Form.svelte";
  import Footer from "../Components/Footer.svelte";

  import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });
</script>

<style>
  iframe {
    width: 100%;
    -webkit-filter: grayscale(100%); /* Conseguimos el color gris */
    -moz-filter: grayscale(100%);
    -ms-filter: grayscale(100%);
    -o-filter: grayscale(100%);
    filter: brightness(0.3);
    transition: var(--transition); /* Apagamos */
  }
  iframe:hover {
    filter: brightness(0.4);
  }
  .contacto {
    flex-direction: column;
    background-color: #35333f;
    padding: 15px;
  }
  .contacto__info {
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    width: 100%;
    background-color: #1d1d1d;
    color: white;
    padding: 20px;
    flex: 1 50%;
  }
  .contacto__info__item--title {
    font-family: "Poppins", sans-serif;
    text-transform: uppercase;
    color: #0884d6;
    font-size: 1.1em;
    margin-bottom: 0px;
  }
  .contacto__info__item--text {
    font-size: 0.9em;
    margin-top: 10px;
    color: white;
  }
   @media screen and (min-width: 1000px){
  .contacto {
      flex-direction: row;
      align-items: initial;
      justify-content: initial;
    }
   }
</style>

<main>

  <section class="mapa">
    <iframe
      title="Google maps"
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3075.3344415159263!2d2.6400387511807444!3d39.5746123142444!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1297925c3c887c0d%3A0xe3778944f65d8bb8!2sCalle%20de%20Sim%C3%B3n%20Ballester%2C%209%2C%2007011%20Palma%2C%20Islas%20Baleares!5e0!3m2!1ses!2ses!4v1591907164636!5m2!1ses!2ses"
      width="800"
      height="500"
      frameborder="0"
      style="border:0;"
      allowfullscreen=""
      aria-hidden="false"
      tabindex="0" />
  </section>
  <section class=" k-grid k-margin k-padding">
    <h1 class="k-title">Ponte en contacto con nosotros</h1>

    <div class="contacto k-flex ">
      <div class="contacto__info">
        <div class="contacto__info__item">
          <p class="contacto__info__item--title">Dirección</p>
          <p class="contacto__info__item--text">
            C/ Simó Ballester nº9, BJ, Palma de mallorca
          </p>
        </div>
        <div class="contacto__info__item">
          <p class="contacto__info__item--title">Teléfono</p>
          <p class="contacto__info__item--text">667634997</p>
        </div>
        <div class="contacto__info__item">
          <p class="contacto__info__item--title">Correo</p>
          <p class="contacto__info__item--text">info@academiamanu.com</p>
        </div>
      </div>
      <Form />
    </div>

  </section>

</main>

<Footer />
