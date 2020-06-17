<script>
  import Form from "../Components/Form.svelte";
  import Footer from "../Components/Footer.svelte";
  import { onMount } from "svelte";
  

  onMount(() => {
    window.scrollTo({
      top: 0,
      left: 0,
      behavior: "smooth"
    });
  });
</script>

<style>
img {
   border-radius: 3px;
}
  /* SECTION BIENVENIDA */
  .s-bienvenida {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    background: url("/assets/banner.jpg");
    background-size: cover;
    background-position: center;
    height: 550px;
    text-align: center;
  }
  .c-bienvenida {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .bienvenida_titulo {
    text-transform: uppercase;
    font-weight: 600;
    font-size: 2.5em;
    padding:0 10px ;
  }
  .bienvenida_subtitulo {
    text-transform: uppercase;
    font-weight: 400;
    font-size: 2em;
  }
  .bienvenida__bg-top {
    position: absolute;
    bottom: 0px;
    width: 100%;
  }
  .bienvenida__bg-top img {
    height: 50px;
  }

  /* SECTION SVGS */
  .c-svg {
    display: grid;
    justify-content: space-evenly;
    flex-wrap: wrap;
    grid-template-columns: repeat(1, 1fr);
  }
  .svg__item {
    background-color: #e2e2e22c;
    display: flex;
    flex-direction: column;
    margin: 0.5rem;
    padding: 10px 2rem;
  }
  .svg__item__img {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .svg__item__img img {
    display: block;
    width: 80px;
  }
  .svg__item__title {
    text-transform: uppercase;
    text-align: center;
    font-size: 1.2em;
  }
  .svg__item__text {
    line-height: 20px;
    font-size: 0.9em;
    text-align: justify;
  }

  /* SECTION BOX */
  .box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .box__img img {
    max-width: 500px;
    min-width: 200px;
  }
  .box__texto {
    text-align: justify;
  }
  .box__texto--content {
    max-width: 600px;
    font-size: 1em;
    color: var(--color-text);
  }
  .box__texto--btn {
    float: right;
  }

  /* SECTION BLOG */
  .c-blog-cards {
    display: grid;
    grid-template-columns: 1fr;
    gap: 5px;
  }
  .blog-card {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 10px 0;
    border-top: 3px solid #e0e0e0;
  }
  .blog-card__img {
    width: 100%;
    object-fit: cover;
    transition: var(--transition);
  }
  .blog-card__img img {
    max-height: 200px;
    object-fit: cover;
  }
  .blog-card__content {
    padding: 0px 10px;
  }
  .blog-card__content--date {
    font-size: 0.7em;
  }
  .blog-card__content--title {
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-size: 0.8em;
    color: #3c3950;
    transition: var(--transition);
    margin: 0;
  }
  .blog-card__content--title:hover {
    color: #0884d6;
  }
  .blog-card__content--text {
    font-size: 0.8em;
  }
  .blog-card__content--widgets {
    display: flex;
  }
  .blog-card__content--widgets > .btn {
    letter-spacing: 0px;
    min-width: 10px;
    margin: 0;
    font-size: 0.8em;
    padding: 2px;
    color: #34b4f0;
    background-color: transparent;
  }
  .blog-card__content--widgets > .btn:hover {
    color: #4b4b4b;
  }
  .blog-card__content--widgets--share {
    cursor: pointer;
    color: #7094ac;
    margin-left: 5px;
    font-size: 1.3em;
    transition: var(--transition);
  }
  .blog-card__content--widgets--share:hover {
    color: #0d4b74;
  }

  /* SECTION REMIUS */
  .s-remius {
    flex-direction: column;
    background: url("/assets/bg-remius.jpg");
    background-size: cover;
  }
  .remius__title {
    font-size: 3em;
    color: white;
    letter-spacing: 1px;
    text-transform: uppercase;
    align-self: center;
    text-align: center;
  }
  .remius__content--text {
    font-size: 1em;
    color: white;
    text-align: justify;
  }

  /* SECTION INSTAGRAM */
  .galeria-insta {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
  }
  .insta_title {
    display: flex;
    align-items: center;
    margin: 10px 0;
  }
  .insta-title__icon {
    margin-right: 5px;
    font-size: 23px;
    background-color: #414141;
    border-radius: 30px;
    padding: 10px 15px;
    color: white;
  }
  .insta-title__text{
    font-size: 1.2em;
  }
  .galeria-insta__item {
    width: 100%;
  }

  /* SECTION CONTACTO */
  .s-contacto {
    background-color: var(--bg-secondary);
  }
  .s-contacto .k-title {
    margin-bottom: 3rem;
  }
  .contacto {
    flex-direction: column;
    background-color: #35333f;
    padding: 20px;
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

  
  @media screen and (min-width: 768px) {
    .c-svg {
      grid-template-columns: repeat(3, minmax(100px, 400px));
    }
    .c-blog-cards {
      grid-template-columns: repeat(2, 1fr);
    }
    .galeria-insta {
      grid-template-columns: repeat(3, 1fr);
    }
    .insta-title__text{
      font-size: 1.5em;
    }
  }
  @media screen and (min-width: 1000px) {
    /* .c-blog-cards {
      grid-template-columns: repeat(3, 1fr);
    } */

    .blog-card {
      grid-template-columns: 1fr 2fr;
    }
    /* SECTION BOX */
    .box {
      flex-direction: row;
    }
    .box__texto {
      padding: 0px 40px;
    }
    /* REMIUS SECTION */
    .c-remius {
      display: flex;
      justify-content: space-evenly;
    }
    .remius__content {
      border-left: 2px solid gray;
      padding: 20px;
      margin-left: 20px;
      max-width: 800px;
    }
    .remius__title {
      justify-self: center;
    }
    .remius__title {
      text-align: center;
    }
    /* CONTACTO SECTION */
    .contacto {
      flex-direction: row;
      align-items: initial;
      justify-content: initial;
    }
  }
  @media screen and (min-width: 1200px) {
    .c-blog-cards {
      grid-template-columns: repeat(3, 1fr);
    }
    .galeria-insta {
      grid-template-columns: repeat(3, minmax(200px, 350px));
    }
  }
</style>

<main>

  <section class="s-bienvenida k-padding">
    <div class="c-bienvenida">
      <h1 class="bienvenida_titulo">
        Formación para el acceso a la policia nacional
      </h1>
      <h2 class="bienvenida_subtitulo">Preparamos tu futuro</h2>
      <button class="btn">Más Información</button>
      <div class="bienvenida__bg-top">
        <img src="assets/bg_bottom.png" alt="" />
      </div>
    </div>

  </section>

  <section class="s-svg k-padding k-margin">
    <div class="c-svg k-grid">
      <div class="svg__item">
        <div class="svg__item__img">
          <img
            src="assets/realiza-examenes.svg"
            alt=""
            style=" margin-left: 1.1rem;" />
        </div>
        <div class="content">
          <h3 class="svg__item__title">Realiza Exámenes</h3>
          <p class="svg__item__text">
            El módulo de exámenes recoge todos los exámenes oficiales desde el
            año 1990 adaptados al temario actual. Te permite hacer simulacros de
            100 preguntas con control de tiempo y archivo de preguntas fallidas.
          </p>
        </div>
      </div>
      <div class="svg__item">
        <div class="svg__item__img">
          <img src="assets/desde-casa.svg" alt="" />
        </div>
        <div class="content">
          <h3 class="svg__item__title">Asiste a clases desde casa</h3>
          <p class="svg__item__text">
            El módulo de exámenes recoge todos los exámenes oficiales desde el
            año 1990 adaptados al temario actual. Te permite hacer simulacros de
            100 preguntas con control de tiempo y archivo de preguntas fallidas.
          </p>
        </div>
      </div>
      <div class="svg__item">
        <div class="svg__item__img">
          <img src="assets/tests-ilimitados.svg" alt="" />
        </div>
        <div class="content">
          <h3 class="svg__item__title">Test ilimitados</h3>
          <p class="svg__item__text">
            El módulo de exámenes recoge todos los exámenes oficiales desde el
            año 1990 adaptados al temario actual. Te permite hacer simulacros de
            100 preguntas con control de tiempo y archivo de preguntas fallidas.
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="k-grid k-margin">
    <div class="box">
      <div class="box__img">
        <img src="assets/info-box-image.jpg" alt="" />
      </div>
      <div class="box__texto">
        <h1 class="box__texto--title k-title">Fórmate con los mejores</h1>
        <div class="box__texto--content">
          <p>
            Todos tenemos nuestro proyecto de vida. No nos damos cuenta pero
            llega un momento en que tenemos que decidir hacia donde orientar
            nuestros esfuerzos.
          </p>
          <p>
            El proyecto de vida personal descansa sobre la elección de pareja,
            amigos y las relaciones con nuestra familia. El proyecto de vida
            profesional se basa en elegir un trabajo que por un lado responda
            mínimamente a nuestros talentos y por otro, nos permita vivir
            dignamente y sustentar a nuestra familia, pero antes de tomar una
            decisión debemos tener en cuenta una serie de consideraciones.
          </p>
        </div>
        <button class="box__texto--btn btn">Más Información</button>
      </div>

    </div>
  </section>

  <section class="blog-bg k-padding k-margin">
    <div class=" k-grid k-margin">
      <h1 class="blog-card--title k-title k-margin">Últimas noticias</h1>
      <div class="c-blog-cards">
        <div class="blog-card">
          <div class="blog-card__img">
            <img src="/assets/ultimas-noticias/SEMINARIO-TEDAX.jpg" alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">27 de enero</span>
            <a href="#/">
              <h1 class="blog-card__content--title">Seminario Tedax - nrbq</h1>
            </a>
            <p class="blog-card__content--text">
              Priximamente iniciaremos de nuevo el ciclo de seminarios
              presenciales de este año 2020.
            </p>
            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img
              src="/assets/ultimas-noticias/SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS.jpg"
              alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">10 de abril</span>
            <a href="#/">
              <h1 class="blog-card__content--title">
                Seminario sobre drogas y drogodepencia
              </h1>
            </a>
            <p class="blog-card__content--text">
              El próximo sábado 27 de abril tendremos el privilegio de contar
              con la presencia del Inspector XXX...
            </p>
            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img src="/assets/ultimas-noticias/OPOCICIONES.jpg" alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">2 de abril</span>
            <a href="#/">
              <h1 class="blog-card__content--title">
                Oposiciones 2019: número de plazas de ingreso en Policía
                Nacional y Guardia Civil
              </h1>
            </a>
            <p class="blog-card__content--text">
              Esta mañana ha salido publicada la relación de plazas tanto para
              el ingreso a la Policía Nacional...
            </p>
            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img src="/assets/ultimas-noticias/LAS-CINCO-DROGAS.jpg" alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">31 de marzo</span>
            <a href="#/">
              <h1 class="blog-card__content--title">
                Las cinco drogas más peligrosas del mundo
              </h1>
            </a>
            <p class="blog-card__content--text">
              El pasado día 29 de marzo pudimos leer una noticia acerca de «
              <a
                href="https://www.policiah50.com/las-cinco-drogas-mas-peligrosas-del-mundo/"
                target="_blank"
                style="display:initial">
                Las cinco drogas más peligrosas del...
              </a>
            </p>

            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img src="/assets/ultimas-noticias/SEMINARIO-TEDAX.jpg" alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">27 de enero</span>
            <a href="#/">
              <h1 class="blog-card__content--title">Seminario Tedax - nrbq</h1>
            </a>
            <p class="blog-card__content--text">
              Priximamente iniciaremos de nuevo el ciclo de seminarios
              presenciales de este año 2020.
            </p>
            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img
              src="/assets/ultimas-noticias/SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS.jpg"
              alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">10 de abril</span>
            <a href="#/">
              <h1 class="blog-card__content--title">
                Seminario sobre drogas y drogodepencia
              </h1>
            </a>
            <p class="blog-card__content--text">
              El próximo sábado 27 de abril tendremos el privilegio de contar
              con la presencia del Inspector XXX...
            </p>
            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img src="/assets/ultimas-noticias/OPOCICIONES.jpg" alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">2 de abril</span>
            <a href="#/">
              <h1 class="blog-card__content--title">
                Oposiciones 2019: número de plazas de ingreso en Policía
                Nacional y Guardia Civil
              </h1>
            </a>
            <p class="blog-card__content--text">
              Esta mañana ha salido publicada la relación de plazas tanto para
              el ingreso a la Policía Nacional...
            </p>
            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
        <div class="blog-card">
          <div class="blog-card__img">
            <img src="/assets/ultimas-noticias/LAS-CINCO-DROGAS.jpg" alt="" />
          </div>
          <div class="blog-card__content">
            <span class="blog-card__content--date">31 de marzo</span>
            <a href="#/">
              <h1 class="blog-card__content--title">
                Las cinco drogas más peligrosas del mundo
              </h1>
            </a>
            <p class="blog-card__content--text">
              El pasado día 29 de marzo pudimos leer una noticia acerca de «
              <a
                href="https://www.policiah50.com/las-cinco-drogas-mas-peligrosas-del-mundo/"
                target="_blank"
                style="display:initial">
                Las cinco drogas más peligrosas del...
              </a>
            </p>

            <div class="blog-card__content--widgets">
              <button class="btn">Leer más</button>
              <div class="blog-card__content--widgets--share">
                <i class="fas fa-share-alt-square" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="s-remius k-padding">
    <div class="c-remius k-grid">
      <h1 class="remius__title">ACCESO ALUMNOS</h1>
      <div class="remius__content">
        <p class="remius__content--text">
          REMIUS es una plataforma virtual de última generación que contiene
          todo lo necesario para preparar la oposición de acceso a la Policía.
          En ella hemos incluido información, materiales pedagógicos, vídeos de
          clases, exámenes, ortografía y psicotécnicos, todo ello bajo el aval
          de una experiencia de más de treinta años. Nuestro sistema de contacto
          te garantiza tener una respuesta sobre cualquier consulta en un máximo
          de 24 horas .
        </p>
        <button class="btn">Accede ya</button>
      </div>
    </div>

  </section>

  <section class="k-flex k-grid k-padding k-margin">
    <div class="c-insta">

      <div class="insta_title">
        <span class="insta-title__icon">
          <i class="fab fa-instagram" />
        </span>
        <h1 class="insta-title__text">@OPOSIPOLACADEMIA</h1>
      </div>

      <div class="galeria-insta">
        <div class="galeria-insta__item">
          <a href="#/">
            <img src="/assets/instagram/1.jpg" alt="" />
          </a>
        </div>
        <div class="galeria-insta__item">
          <a href="#/">
            <img src="/assets/instagram/2.jpg" alt="" />
          </a>
        </div>
        <div class="galeria-insta__item">
          <a href="#/">
            <img src="/assets/instagram/3.jpg" alt="" />
          </a>
        </div>
        <div class="galeria-insta__item">
          <a href="#/">
            <img src="/assets/instagram/4.jpg" alt="" />
          </a>
        </div>
        <div class="galeria-insta__item">
          <a href="#/">
            <img src="/assets/instagram/5.jpg" alt="" />
          </a>
        </div>
        <div class="galeria-insta__item">
          <a href="#/">
            <img src="/assets/instagram/6.jpg" alt="" />
          </a>
        </div>
      </div>
    </div>

  </section>

  <section class="s-contacto k-padding ">
    <div class="c-contacto k-grid">
      <h1 class="k-title">Contacto</h1>
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

    </div>

  </section>
</main>

<Footer />
