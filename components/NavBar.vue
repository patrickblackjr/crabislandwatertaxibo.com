<template>
  <div id="navigation">
    <b-container>
      <b-navbar exact class="sticky-top" toggleable="md" type="dark" variant="dark">

        <b-navbar-toggle exact target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="/"><img src="@/assets/logo.png"></b-navbar-brand>

        <b-collapse is-nav id="nav_collapse">

          <b-navbar-nav class="ml-auto">
            <b-nav-item exact to="/">Home</b-nav-item>
            <b-nav-item-dropdown exact text="Firestopping">
              <b-dropdown-item exact to="/firestopping">Firestopping</b-dropdown-item>
              <b-dropdown-item exact to="/about-us">About Us</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item exact to="/contact">Contact</b-nav-item>
            <b-nav-item exact to="/services">Services</b-nav-item>
            <b-nav-item exact to="/safety">Safety</b-nav-item>
            <b-nav-item exact to="/bid-request">Bid Request</b-nav-item>
          </b-navbar-nav>

      </b-collapse>
      </b-navbar>
    </b-container>
  </div>
</template>

<style>
#navigation {
  background-color: #343A40;
}
</style>