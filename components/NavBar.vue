<template>
  <div id="navigation">
    <b-container>
      <b-navbar
        v-b-scrollspy:main
        fixed="top"
        class=""
        toggleable="md"
        type="dark"
        variant="dark"
      >
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="/"
          ><img height="40" src="@/assets/logo-color-light.png"
        /></b-navbar-brand>

        <b-collapse id="nav_collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="#home">Home</b-nav-item>
            <b-nav-item href="#rates">Rates</b-nav-item>
            <b-nav-item href="#about">About</b-nav-item>
            <b-nav-item href="#contact">Contact</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </b-container>
  </div>
</template>

<style lang="scss" scoped>
$yellow: #ffcb00;

#navigation {
  background-color: #343a40;
}
.navbar-nav .active > .nav-link {
  color: $yellow;
}
</style>
