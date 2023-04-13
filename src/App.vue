<template>
  <head>
    <title>Mi página informativa</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header>
      <img
        src="data:image/png;base64,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"
        alt=""
      />
      <h1>BANCO NACIONAL DE BOLIVIA</h1>
      <nav>
        <ul>
          <li><a href="#seccion1">Sección 1</a></li>
          <li><a href="#seccion2">Sección 2</a></li>
          <li><a href="#seccion3">Sección 3</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <section id="seccion1">
        <h2>Responsabilidad Social</h2>
        <div>
                <div>
                <img
          src="https://www.bnb.com.bo/PortalBNB/Images/Rse/BannerReducido/Mini-banner-rse.jpg"
          alt=""
        />
        </div>
            <div> 
        <p>
          El Banco Nacional de Bolivia S.A. (BNB) se caracteriza por ser una
          institución sólida que invariablemente ha actuado eficiente,
          responsable y transparentemente frente a sus accionistas y clientes,
          procurando el desarrollo profesional y personal de sus funcionarios y
          ejecutando proyectos sociales con miras a contribuir al desarrollo del
          país.
        </p>
        </div>

        </div>

      </section>
      <section id="seccion2">
        <h2>Servcios que Ofrecemos</h2>
        <img src="https://www.bnb.com.bo/PortalBNB/Images/BienesAdjudicados/Banners/Mini-banner-bienes.jpg" alt="">
        <p>
          Los servicios que ofrece incluyen cuentas de ahorros, tarjetas de
          crédito, hipotecas, préstamos comerciales y asesoría financiera y de
          inversiones. El Banco Nacional de Bolivia pertenece al Grupo BNB y
          posee cuatro filiales: BNB Safi, BNB Valores, BNB Valores Perú y BNB
          Leasing.
        </p>
      </section>
      <section id="seccion3">
        <h2>Educación Financiera</h2>
        <img src="https://www.bnb.com.bo/PortalBNB/Images/Personas/BannerReducido/Mini_banner_Educaci%c3%b3n_Financiera.jpeg" alt="">
        <p>El programa de Educación Financiera, Aprendiendo con el BNB, tiene el objetivo de mejorar la cultura financiera de los bolivianos, dotándoles de información y herramientas necesarias para que administren sus finanzas de forma responsable y segura, promoviendo, de esta manera, el uso de todos los productos y servicios bancarios que se ofrecen en el sistema financiero.</p>
      </section>
    </main>
    <footer>
      <p>hola mundo de banco vue &copy; 2023</p>
    </footer>
  </body>
</template>

<script>
export default {
  name: 'App',
  components: {},
};
</script>

<style>
/* Estilos para el encabezado */
header {
  background-color: green;
  color: #fff;
  padding: 20px;
  text-align: center;
}

/* Estilos para el título */
h1 {
  font-size: 36px;
  margin: 0;
}

/* Estilos para el menú de navegación */
nav {
  background-color: #b600fb;
  margin-top: 20px;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

nav li {
  display: inline-block;
  margin-right: 20px;
}

nav a {
  color: #fff;
  text-decoration: none;
}

nav a:hover {
  text-decoration: underline;
}

/* Estilos para las secciones */
section {
  padding: 20px;
}

section h2 {
  font-size: 24px;
  margin-top: 0;
}

/* Estilos para el pie de página */
footer {
  background-color: green;
  padding: 10px;
  text-align: center;
  color:white;
}
</style>
