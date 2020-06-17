<script>
  import { onMount } from "svelte";

  import { Router, Link, Route } from "svelte-routing";
  import Contacto from "./routes/Contacto.svelte";
  import Cursos from "./routes/Cursos.svelte";
  import Home from "./routes/Home.svelte";
  import Noticias from "./routes/Noticias.svelte";

  import * as animateScroll from "svelte-scrollto";

  export let url = "";
  let active = false;
  let sideEstado = false;
  let s_body = document.body.style;

  onMount(() => {
    let links = document.querySelectorAll(".sidebar_nav__items");
    let sidebar = document.querySelector(".sidebar");
    let barra = document.querySelector(".btn-barra");

    links.forEach(link => {
      console.log(link);
      link.addEventListener("click", closeSideBar);
    });
    console.log(links);

    window.scrollTo(0, 0);

    window.addEventListener("click", e => {
      console.log(e.target);
      if (e.target != barra && e.target != sidebar) {
        closeSideBar();
      }
    });
  });

  const toggleSideBar = () => {
    sideEstado = !sideEstado;
  };
  const closeSideBar = () => {
    sideEstado = false;
  };
</script>

<style>
  header {
    position: fixed;
    display: flex;
    align-items: center;
    box-sizing: border-box;
    width: 100%;
    top: 0;
    background-color: black;
    z-index: 1111;
    min-height: 80px;
  }
  .contenedor-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1200px;
    width: 100%;
  }

  a {
    display: block;
    text-decoration: none;
  }

  nav {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .c-logo__img {
    display: block;
    max-width: 230px;
  }

  .menu {
    border-radius: 3px;
    display: flex;
  }

  #barra i {
    display: none;
    font-size: 1.7rem;
    color: white;
    cursor: pointer;
  }

  .sidebar {
    position: absolute;
    top: 80px;
    left: 0;
    background-color: rgb(0, 0, 0);
    display: flex;
    width: 100%;
    flex-direction: column;
    transition: var(--transition);
    padding: 15px 0px;
    transform: translate3d(-500%, 0, 0);
  }

  .icon-moodle {
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    background-color: #2697d8;
    border: 2px solid #dfdfdf;
    border-radius: 30px;

    padding: 15px 20px;
    transition: var(--transition);
  }
  .icon-moodle span {
    margin-left:10px;
    text-transform: uppercase;
    text-align: center;
    font-weight: 500;
    font-size: 0.8em;
  }
  .icon-moodle:hover {
    background-color: #caa339;
  }

  .active {
    transform: translate3d(0%, 0, 0);
  }
  @media screen and (max-width: 500px) {
    .icon-moodle {
      padding: 10px;
      font-size: 0.8em
    }
    
    .c-logo__img {
      max-width: 160px;
    }
  }
  @media only screen and (max-width: 1000px) {
    #barra i {
      display: block;
    }

    .menu {
      display: none;
    }

    nav {
      justify-content: space-between;
    }

    
  }

  @media only screen and (min-width: 1000px) {
    .sidebar {
      display: none !important;
    }
  }
</style>

<Router {url}>
  <header>
    <div class="contenedor-header k-grid">

      <div id="barra">
        <i class="fas fa-bars btn-barra" on:click={toggleSideBar} />
      </div>
      <nav>
        <div class="menu">
          <div class="menu__items">
            <Link to="/">Inicio</Link>
          </div>
          <div class="menu__items">
            <Link to="cursos">Cursos</Link>
          </div>

        </div>
        <div class="c-logo">
          <Link to="/">
            <img
              class="c-logo__img"
              src="assets/logo-negro.png"
              alt="logo-oposipol" />
          </Link>
        </div>

        <div class="menu">
          <div class="menu__items">
            <Link to="contacto">Contacto</Link>
          </div>
          <div class="menu__items">
            <Link to="noticias">Noticias</Link>
          </div>

        </div>

      </nav>
      <a
        href="http://pruebas.oposipolacademia.com/moodle-kevin/moodle/login/index.php">
        <div class="icon-moodle">
          <i class="fas fa-user-graduate"></i>
          <span>Acceso Alumnos</span>
        </div>
      </a>
      <div class="sidebar" class:active={sideEstado}>
        <!-- <div class="sidebar_btn" on:click={closeSideBar}>
        <i class="fas fa-arrow-left" />
      </div> -->
        <div class="sidebar_nav">
          <div class="sidebar_nav_items">
            <Link to="/">Inicio</Link>
          </div>
          <div class="sidebar_nav_items">
            <Link to="cursos">Cursos</Link>
          </div>
          <div class="sidebar_nav_items">
            <Link to="contacto">Contacto</Link>
          </div>
          <div class="sidebar_nav_items">
            <Link to="noticias">Noticias</Link>
          </div>
          <div class="sidebar_nav_items">
            <Link to="remius">
              Acceso alumnos
              <i class="fas fa-sign-in-alt" />
            </Link>
          </div>
        </div>
      </div>
    </div>
  </header>
  <button class="btn-scrollTop" on:click={() => animateScroll.scrollToTop()}>
    <i class="fas fa-chevron-up" />
  </button>
  <Route path="contacto" component={Contacto} />
  <Route path="noticias" component={Noticias} />
  <Route path="cursos" component={Cursos} />
  <Route path="/">
    <Home />
  </Route>

</Router>
