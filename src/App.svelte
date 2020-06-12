<script>
  import { onMount } from "svelte";

  import { Router, Link, Route } from "svelte-routing";
  import Contacto from "./routes/Contacto.svelte";
  import Cursos from "./routes/Cursos.svelte";
  import Home from "./routes/Home.svelte";

  import * as animateScroll from "svelte-scrollto";

  export let url = "";

  let sideEstado = false;
  let s_body = document.body.style;
  let menu__items = "menu__items";

  onMount(() => {
    let links = document.querySelectorAll(".menu__items");
    links.forEach(link => {
      console.log(link);
      link.addEventListener("click", closeSideBar);
    });
    console.log(links);

    window.scrollTo(0, 0);
  });

  const openSideBar = () => {
    sideEstado = true;
  };
  const closeSideBar = () => {
    sideEstado = false;
  };

  $: {
    sideEstado ? (s_body.overflow = "hidden") : (s_body.overflow = "initial");
    window.location.href;
  }
</script>

<style>
  header {
    position: fixed;
    width: 100%;
    background-color: black;
    z-index: 1111;
  }

  a {
    display: block;
    text-decoration: none;
  }

  nav {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0px 50px;
  }

  .c-logo__img {
    display: block;
    width: 230px;
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
    top: 0;
    bottom: 0;
    display: flex;
    width: 100%;
    height: 100vh;
    flex-direction: column;
    background-color: black;
    transition: var(--transition);
    transform: translate3d(-100%, 0, 0);
  }

  .sidebar_btn {
    background-color: #353535;
  }

  .sidebar_btn i {
    cursor: pointer;
    font-size: 20px;
    padding: 10px;
    color: rgb(53, 53, 53);
    background-color: #2697d8;
  }

  .sidebar_btn i:hover {
    background-color: #2697d8a9;
  }

  .icon-moodle {
    position: relative;
    right: -30px;
    background-color: #2697d8;
    color: white;
    border-color: 2px solid #2697d8;
    border-radius: 20px;
    width: 60px;

    padding: 10px 20px;
    transition: var(--transition);
  }
  .icon-moodle h1 {
    margin: 0;
    text-transform: uppercase;
    text-align: center;
    margin: 0;
    font-weight: 500;
    font-size: 11px;
  }
  .icon-moodle:hover {
    background-color: #01779e;
    border: 1px solid white;
  }

  .active {
    transform: translate3d(0%, 0, 0);
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

    .c-logo__img {
      width: 200px;
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
    <nav>
      <div class="menu">
        <Link clase={menu__items} to="/">Inicio</Link>
        <Link clase={menu__items} to="cursos">Cursos</Link>

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
        <Link clase={menu__items} to="contacto">Contacto</Link>
        <Link clase={menu__items} to="noticias">Noticias</Link>

      </div>

      <div id="barra" on:click={openSideBar}>
        <i class="fas fa-bars" />
      </div>
      <a href="/">
        <div class="icon-moodle">
          <h1>Acceso Alumnos</h1>
        </div>
      </a>

    </nav>
    <div class="sidebar" class:active={sideEstado == true ? 'active' : ''}>
      <div class="sidebar_btn" on:click={closeSideBar}>
        <i class="fas fa-arrow-left" />
      </div>
      <div class="sidebar_nav">
        <Link to="/" clase={'sidebar_nav__items'}>Inicio</Link>
        <Link to="cursos" clase={'sidebar_nav__items'}>Cursos</Link>
        <Link to="contacto" clase={'sidebar_nav__items'}>Contacto</Link>
        <Link to="noticias" clase={'sidebar_nav__items'}>Noticias</Link>
        <Link to="remius" clase={'sidebar_nav__items'}>
          Remius
          <i class="fas fa-sign-in-alt" />
        </Link>
      </div>
    </div>
  </header>
  <button class="btn-scrollTop" on:click={() => animateScroll.scrollToTop()}>
    <i class="fas fa-chevron-up" />
  </button>
  <Route path="contacto" component={Contacto} />
  <Route path="cursos" component={Cursos} />
  <Route path="/">
    <Home />
  </Route>

</Router>
