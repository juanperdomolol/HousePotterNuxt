<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark" >
      <b-navbar-brand href="/">
        <img
          src="https://www.juguemay.com/wp-content/uploads/2019/01/PRINCIPAL-1024x419.jpg"
          width="90px"
        />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav mr-5>
          <b-nav-item href="/personajes">Personajes</b-nav-item>
          <b-nav-item href="/estudiantes">Estudiantes</b-nav-item>
          <b-nav-item href="/profesores">Profesores</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>