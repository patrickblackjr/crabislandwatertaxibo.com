<template>
  <div id="home" class="h-100 justify-content-center align-items-center">
    <div class="layer"></div>
    <h1 class="text-white text-center hero-text">
      Water Taxi to Crab Island
    </h1>
  </div>
</template>

<style lang="scss" scoped>
#home {
  background-image: linear-gradient(
      to right,
      rgba(2, 170, 176, 0.75),
      rgba(0, 205, 172, 0.75)
    ),
    url(~assets/main.jpg);
  height: 100%;
  width: 100%;
  min-height: 90vh;
  margin: 0;
  background-size: cover;
  background-position: center center;
  display: flex;
}
h1 {
  font-weight: 600;
}
.hero-text {
  font-size: 4rem;
  text-shadow: 0px 0px 11px rgba(0, 0, 0, 0.5);
}
</style>
