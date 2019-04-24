<template>
  <div id="navigation">
    <b-container>
      <b-navbar
        v-b-scrollspy:nav-scroller
        exact
        sticky
        class=""
        toggleable="md"
        type="dark"
        variant="dark"
      >
        <b-navbar-toggle exact target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="/"
          ><img height="40" src="@/assets/logo-color-light.png"
        /></b-navbar-brand>

        <b-collapse id="nav_collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item exact href="#home" @click="scrollIntoView"
              >Home</b-nav-item
            >
            <b-nav-item exact href="#rates" @click="scrollIntoView"
              >Rates</b-nav-item
            >
            <b-nav-item exact href="#about" @click="scrollIntoView"
              >About</b-nav-item
            >
            <b-nav-item exact href="#contact" @click="scrollIntoView"
              >Contact</b-nav-item
            >
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </b-container>
  </div>
</template>

<style lang="scss" scoped>
#navigation {
  background-color: #343a40;
}
</style>
