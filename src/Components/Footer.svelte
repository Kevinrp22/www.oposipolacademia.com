<script>

</script>

<style>
  .footer-margin {
  }
  .c-footer {
    color: white;
    font-size: 0.9em;
  }
  .footer__1 {
    display: grid;
    grid-template-columns: 1fr;
    color: white;
  }

  .footer__1__contacto--title {
    text-transform: uppercase;
    font-size: 1.5em;
  }
  .footer__1__contacto--text {
    color: white;
  }

  .footer__1__contacto--item {
    display: flex;
    margin-bottom: 10px;
  }
  .footer__1__contacto--item span {
    margin-right: 10px;
    color: #0884d6;
  }

  .footer__2 {
    display: flex;
    justify-content: space-evenly;
    margin: 2rem 0;
  }
  .footer__2__item {
    margin: 0px 5px;
    color: white;
    transition: var(--transition);
  }
  .footer__2__item:hover {
    color: #0884d6;
  }
  .footer__2__item:last-child {
    margin-right: 0px;
  }
  .footer__2__item:first-child {
    margin-left: 0px;
  }

  .footer__separador {
    margin: 15px 0px;
    border-bottom: 4px solid gray;
  }
  .footer__4 {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }
  .footer__4__copy {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }
  .footer__4__rrrss {
    display: flex;
    justify-content: space-evenly;
    margin: 2rem 0;
  }
  .footer__4__rrrss a {
    font-size: 1.5em;
    transition: var(--transition);
    padding: 10px;
  }
  .footer__4__rrrss a:hover {
    color: white !important;
  }

  .footer__4__img {
    width: 150px;
  }
  .footer__4 p {
    color: white;
    font-size: 0.8em;
  }

  /* RECORDATORIO TERMINAR RESPONSIVE DEL FOOTER */
  @media screen and (min-width: 768px) {
    .footer__1 {
      grid-template-columns: repeat(2, 1fr);
      justify-content: space-between;
      padding: 0 30px;
    }
    .footer__1__quienes-somos {
      max-width: 400px;
    }
    .footer__4 {
      display: flex;
      flex-direction: row-reverse;
      justify-content: space-around;
    }
    .footer__1__contacto {
      justify-self: center;
    }
  }
  @media screen and (min-width: 1000px) {
  }
  @media screen and (min-width: 1200px) {
  }
</style>

<div class="c-footer k-grid k-padding">
  <div class="footer__1">
    <div class="footer__1__quienes-somos">
      <h1 class="footer__1__contacto--title">Quienes somos</h1>
      <p class="footer__1__contacto--text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus
        error officiis nemo, illum culpa esse consequuntur. Sapiente, minima
        qui. Assumenda, explicabo corrupti iste pariatur dolores officiis!
        Mollitia autem explicabo nam!
      </p>
      <img src="assets/logo-blanco-slim.png" alt="" />
    </div>

    <div class="footer__1__contacto">
      <h1 class="footer__1__contacto--title">Contacto</h1>
      <div class="footer__1__contacto--item">
        <span>
          <i class="fas fa-map-marker-alt" />
        </span>
        C/ Simó Ballester nº9 BJ, Palma de Mallorca
      </div>
      <div class="footer__1__contacto--item">
        <span>
          <i class="fas fa-phone-square-alt" />
        </span>
        667 634 997
      </div>
      <div class="footer__1__contacto--item">
        <span>
          <i class="far fa-envelope" />
        </span>
        info@academiamanu.com
      </div>
    </div>
  </div>
  <div class="footer__2 footer-margin">
    <a href="#/" class="footer__2__item">INICIO</a>
    |
    <a href="#/" class="footer__2__item">CURSOS</a>
    |
    <a href="#/" class="footer__2__item">CONTACTO</a>
    |
    <a href="#/" class="footer__2__item">NOTICIAS</a>
    |
    <a href="#/" class="footer__2__item">MOODLE</a>
  </div>

  <div class="footer__separador" />

  <div class="footer__4 footer-margin">
    <div class="footer__4__rrrss footer-margin">
      <a href="#/" style="color:#4064ad">
        <i class="fab fa-facebook-f" />
      </a>
      <a href="#/" style="color:#1c9deb">
        <i class="fab fa-twitter" />
      </a>
      <a href="#/" style="color:#eb552a">
        <i class="fab fa-instagram" />
      </a>
      <a href="#/" style="color:#f80000">
        <i class="fab fa-youtube" />
      </a>
    </div>
    <div class="footer__4__copy">
      <img src="assets/logo-negro.png" alt="" class="footer__4__img" />
      <p>
        2017 © Copyright Academia Oposipol
        <br />
        Todos los derechos reservados
      </p>
    </div>
  </div>
</div>
l
