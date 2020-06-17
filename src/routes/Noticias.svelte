<script>
  import Footer from "../Components/Footer.svelte";
  const posts = [
    {
      id: 1,
      date: "27 de enero",
      img: "/assets/ultimas-noticias/SEMINARIO-TEDAX.jpg",
      title: "Seminario Tedax - nrbq",
      content:
        "Priximamente iniciaremos de nuevo el ciclo de seminarios presenciales de este año 2020. Este formato de charlas para acercar el trabajo de distintas unidades de la Policía Nacional, tuvo una gran acogida el año pasado . "
    },
    {
      id: 2,
      date: "2 de abril",
      img: "/assets/ultimas-noticias/OPOCICIONES.jpg",
      title:
        "OPOSICIONES 2019: NÚMERO DE PLAZAS DE INGRESO EN POLICÍA NACIONAL Y GUARDIA CIVIL ",
      content:
        "Esta mañana ha salido publicada la relación de plazas tanto para el ingreso a la Policía Nacional como en la Guardia Civil para este año. "
    },
    {
      id: 3,
      date: "10 de abril",
      img: "/assets/ultimas-noticias/SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS.jpg",
      title: "SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS",
      content:
        "El próximo sábado 27 de abril tendremos el privilegio de contar con  la presencia del Inspector XXX, actual Jefe del Grupo de  Estupefacientes de la Jefatura Superior de Policía de Balearespara  impartir en nuestras aulas de un Seminario presencial para acercarnos el  trabajo de este grupo a los opositores de Policía Nacional"
    },
    {
      id: 4,
      date: "27 de enero",
      img: "/assets/ultimas-noticias/LAS-CINCO-DROGAS.jpg",
      title: "LAS CINCO DROGAS MÁS PELIGROSAS DEL MUNDO",
      content:
        "El pasado día 29 de marzo pudimos leer una noticia acerca de «Las cinco  drogas más peligrosas del mundo» en el periódico policial PoliciaH50 y  creímos que sería interesante compartirlo con todos vosotros"
    },
    {
      id: 1,
      date: "27 de enero",
      img: "/assets/ultimas-noticias/SEMINARIO-TEDAX.jpg",
      title: "Seminario Tedax - nrbq",
      content:
        "Priximamente iniciaremos de nuevo el ciclo de seminarios presenciales de este año 2020. Este formato de charlas para acercar el trabajo de distintas unidades de la Policía Nacional, tuvo una gran acogida el año pasado . "
    },
    {
      id: 2,
      date: "2 de abril",
      img: "/assets/ultimas-noticias/OPOCICIONES.jpg",
      title:
        "OPOSICIONES 2019: NÚMERO DE PLAZAS DE INGRESO EN POLICÍA NACIONAL Y GUARDIA CIVIL ",
      content:
        "Esta mañana ha salido publicada la relación de plazas tanto para el ingreso a la Policía Nacional como en la Guardia Civil para este año. "
    },
    {
      id: 3,
      date: "10 de abril",
      img: "/assets/ultimas-noticias/SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS.jpg",
      title: "SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS",
      content:
        "El próximo sábado 27 de abril tendremos el privilegio de contar con  la presencia del Inspector XXX, actual Jefe del Grupo de  Estupefacientes de la Jefatura Superior de Policía de Balearespara  impartir en nuestras aulas de un Seminario presencial para acercarnos el  trabajo de este grupo a los opositores de Policía Nacional"
    },
    {
      id: 4,
      date: "27 de enero",
      img: "/assets/ultimas-noticias/LAS-CINCO-DROGAS.jpg",
      title: "LAS CINCO DROGAS MÁS PELIGROSAS DEL MUNDO",
      content:
        "El pasado día 29 de marzo pudimos leer una noticia acerca de «Las cinco  drogas más peligrosas del mundo» en el periódico policial PoliciaH50 y  creímos que sería interesante compartirlo con todos vosotros"
    },
    {
      id: 1,
      date: "27 de enero",
      img: "/assets/ultimas-noticias/SEMINARIO-TEDAX.jpg",
      title: "Seminario Tedax - nrbq",
      content:
        "Priximamente iniciaremos de nuevo el ciclo de seminarios presenciales de este año 2020. Este formato de charlas para acercar el trabajo de distintas unidades de la Policía Nacional, tuvo una gran acogida el año pasado . "
    },
    {
      id: 2,
      date: "2 de abril",
      img: "/assets/ultimas-noticias/OPOCICIONES.jpg",
      title:
        "OPOSICIONES 2019: NÚMERO DE PLAZAS DE INGRESO EN POLICÍA NACIONAL Y GUARDIA CIVIL ",
      content:
        "Esta mañana ha salido publicada la relación de plazas tanto para el ingreso a la Policía Nacional como en la Guardia Civil para este año. "
    },
    {
      id: 3,
      date: "10 de abril",
      img: "/assets/ultimas-noticias/SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS.jpg",
      title: "SEMINARIO-DROGAS-Y-DROGODEPENDENCIAS",
      content:
        "El próximo sábado 27 de abril tendremos el privilegio de contar con  la presencia del Inspector XXX, actual Jefe del Grupo de  Estupefacientes de la Jefatura Superior de Policía de Balearespara  impartir en nuestras aulas de un Seminario presencial para acercarnos el  trabajo de este grupo a los opositores de Policía Nacional"
    },
    {
      id: 4,
      date: "27 de enero",
      img: "/assets/ultimas-noticias/LAS-CINCO-DROGAS.jpg",
      title: "LAS CINCO DROGAS MÁS PELIGROSAS DEL MUNDO",
      content:
        "El pasado día 29 de marzo pudimos leer una noticia acerca de «Las cinco  drogas más peligrosas del mundo» en el periódico policial PoliciaH50 y  creímos que sería interesante compartirlo con todos vosotros"
    }
  ];
</script>

<style>
  /* SECTION BLOG */
  main {
    padding-top: 190px;
  }

  .k-grid {
    max-width: 1200px;
  }
  .bg {
    background-color: #e6e9ee;
  }
  .filter {
    display: flex;
    justify-content: space-between;
    background-color: #ffffff;
    margin: 10px 0;
    padding: 20px;
  }
  .busqueda {
    position: relative;
  }
  .busqueda i {
    position: absolute;
    top: 9px;
    right: 10px;
  }
  .ordenar {
    display: flex;
    align-items: center;
  }
  .ordenar span{
    margin-right: 10px;
  }

  .contenido-principal {
    display: grid;
    grid-template-columns: 3fr 1fr;
    gap: 0 20px;
  }
  .content {
    background-color: white;
  }

  .c-blog-cards {
    display: grid;
    grid-template-columns: 1fr;
    gap: 5px;
    padding: 30px;
  }
  .blog-card {
    min-width: 100px;
    padding: 10px;
    align-content: flex-start;
    background-color: #f3f3f3e3;
    border-bottom: 1px solid rgb(248, 248, 248);
    border-radius: 4px;
    transition: var(--transition);
  }
  .blog-card a {
    height: 100%;
  }
  .blog-card:hover {
    background-color: #bdbdbd;
  }
  .blog-card__img {
    width: 100%;
    object-fit: cover;
    transition: var(--transition);
    filter: brightness(0.8);
  }
  .blog-card__img img {
    object-fit: cover;
    height: 220px;
  }
  .blog-card__content {
    padding: 10px 5px;
  }
  .blog-card__header {
    min-height: 150px;
  }
  .blog-card__header--date {
    font-size: 1em;
    margin: 10px 0 20px;
    font-weight: 700;
    color: #606c7e;
    text-transform: uppercase;
  }
  .blog-card__header--title {
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-size: 1.3em;
    color: #3c3950;
    transition: var(--transition);
    margin: 0;
  }
  .blog-card__header--title:hover {
    color: #0884d6;
  }

  .blog-card__content--text {
    font-size: 0.9em;
    text-align: justify;
  }
  .blog-card__content--widgets {
    display: flex;
  }
  .blog-card__content--widgets > .btn {
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

  .blog-sidebar {
    display: flex;
    align-items: flex-end;
    flex-direction: column;
  }
  .blog-sidebar__item {
    box-sizing: border-box;
    padding: 20px;
    background-color: white;
    max-width: 280px;
    margin-bottom: 20px;
  }
  .blog-sidebar__item__title {
    font-size: 1.5em;
    text-transform: uppercase;
    text-align: center;
    width: 100%;
  }

  @media screen and (max-width: 768px) {
    .ordenar span {
      display: none;
    }
    .blog-sidebar {
      display: none;
    }
    .contenido-principal {
      grid-template-columns: 1fr;
    }
  }
  @media screen and (min-width: 1000px) {
    .c-blog-cards {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  @media screen and (min-width: 2100px) {
    .k-grid {
      max-width: 1600px;
    }
    .c-blog-cards {
      grid-template-columns: repeat(3, 1fr);
    }
    .contenido-principal {
      grid-template-columns: 4fr 1fr;
    }
  }
</style>

<div class="bg">
  <main class="page">
    <div class="k-grid">
      <div class="filter">
        <div class="busqueda">
          <input type="text" placeholder="Buscar" />
          <i class="fas fa-search" />
        </div>
        <div class="ordenar">
          <span>OORDENAR POR</span>
          <select name="" id="">
            <option value="">Orden Alb. Ascendente</option>
            <option value="">Orden Alb. Descendente</option>
            <option value="">Novedades</option>
          </select>
        </div>
      </div>
      <div class="contenido-principal">
        <div class="content">
          <div class="c-blog-cards">

            {#each posts as post}
              <div class="blog-card">
                <a href="#/">
                  <div class="blog-card__header">
                    <a href="#/">
                      <h1 class="blog-card__header--title">{post.title}</h1>
                    </a>
                    <p class="blog-card__header--date">{post.date}</p>
                  </div>

                  <div class="blog-card__img">
                    <img src={post.img} alt="" />
                  </div>

                  <div class="blog-card__content">
                    <p class="blog-card__content--text">{post.content}</p>
                    <div class="blog-card__content--widgets">
                      <button class="btn">Leer más</button>
                      <div class="blog-card__content--widgets--share">
                        <i class="fas fa-share-alt-square" />
                      </div>
                    </div>
                  </div>
                </a>
              </div>
            {/each}

          </div>
        </div>
        <div class="blog-sidebar">
          <div class="blog-sidebar__item">
            <h1 class="blog-sidebar__item__title">Facebook</h1>
            <iframe
              title="facebook"
              src="//www.facebook.com/plugins/likebox.php?href=https%3A%2F%2Fwww.facebook.com%2FProfesorCNP%2F&amp;width=240&amp;height=230&amp;show_faces=true&amp;colorscheme=light&amp;stream=false&amp;show_border=false&amp;header=false"
              scrolling="no"
              frameborder="0"
              style="border:none; overflow:hidden; width:240px; height:250px;
              vertical-align: top;"
              allowtransparency="true" />
          </div>
          <div class="blog-sidebar__item">
            <h1 class="blog-sidebar__item__title">Algunos videos</h1>

            <iframe
              title="videoYT1"
              width="100%"
              src="https://www.youtube.com/embed/yk48m7Rgr-Y"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope;
              picture-in-picture"
              allowfullscreen />

            <iframe
              title="videoYT2"
              width="100%"
              src="https://www.youtube.com/embed/XBux7GHQw2U"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope;
              picture-in-picture"
              allowfullscreen />
          </div>
        </div>
      </div>
    </div>

  </main>
</div>
<Footer />
