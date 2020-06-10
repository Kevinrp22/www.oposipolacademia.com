<script>
  import {
    onMount
  } from "svelte";
  import {
    Router,
    Link,
    Route
  } from "svelte-routing";
  import Contacto from "./routes/Contacto.svelte";
  import Cursos from "./routes/Cursos.svelte";
  import Home from "./routes/Home.svelte";

  export let url = "";

  let sideEstado = false;
  let s_body = document.body.style;

  onMount(() => {
    let links = document.querySelectorAll(".menu__items");
    links.forEach(link => {
      console.log(link);
      link.addEventListener("click", closeSideBar);
    });
    console.log(links);
  });

  const openSideBar = () => {
    sideEstado = true;
  };
  const closeSideBar = () => {
    sideEstado = false;
  };

  $: sideEstado ? s_body.overflow = "hidden": s_body.overflow = "initial" 
  
</script>

<Router {url}>
  <header>
    <nav>
      <div class="menu">
        <Link to="/">Home</Link>
        <Link to="cursos">Cursos</Link>
        <Link to="contacto">Contacto</Link>
      </div>
      <div class="c-logo">
        <Link to="/">
        <img class="c-logo__img" src="assets/logo-negro.png" alt="logo-oposipol" />
        </Link>
      </div>

      <div class="menu">
        <Link to="noticias">Noticias</Link>
        <Link to="remius">
        Remius
        <i class="fas fa-sign-in-alt" />
        </Link>

      </div>

      <div id="barra" on:click={openSideBar}>
        <i class="fas fa-bars" />
      </div>

    </nav>
    <div class="sidebar" class:active={sideEstado==true ? 'active' : '' }>
      <div class="sidebar_btn" on:click={closeSideBar}>
        <i class="fas fa-arrow-left" />
      </div>
      <div class="sidebar_nav">
        <Link to="/">Home</Link>
        <Link to="cursos" class="sidebar_nav__items">Cursos</Link>
        <Link to="contacto" class="sidebar_nav__items">Contacto</Link>
        <Link to="noticias" class="sidebar_nav__items">Noticias</Link>
        <Link to="remius" class="sidebar_nav__items">
        Remius
        <i class="fas fa-sign-in-alt" />
        </Link>
      </div>
    </div>
  </header>
  <Route path="contacto" component={Contacto} />
  <Route path="cursos" component={Cursos} />
  <Route path="/">
    <Home />
  </Route>
</Router>


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
    overflow: hidden;
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

  .sidebar_nav__items {
    display: flex;
    color: #ffffff;
    background-color: #353535;
    text-transform: uppercase;
    font-weight: 500;
    font-size: 0.9em;
    padding: 20px;
    margin: 0.9px 0px;
    transition: var(--transition);
  }

  .sidebar_nav__items i {
    font-size: 0.9rem;
    color: white;
    margin-left: 10px;
    transition: var(--transition);
  }

  .sidebar_nav__items:hover {
    color: #2697d8;

    background-color: #4d4d4d;
  }

  .sidebar_nav__items:hover>i {
    color: #2697d8;
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
    .menu-desplegable {
      display: none !important;
    }
  }
</style>