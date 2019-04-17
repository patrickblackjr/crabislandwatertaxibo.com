<template>
<div>

  <div v-if="error.statusCode === 404">
    <div class="container text-center mt-5">
      <h2>404 Error</h2>
      <p>Uh oh! That page couldn't be found.</p>
      <b-btn to="/" variant="primary">Back to the homepage</b-btn>
    </div>
  </div>

  <div v-if="error.statusCode === 500">
    <div class="container text-center mt-5">
      <h2>500 Error</h2>
      <p>We seem to having some server issues. Check back soon</p>
    </div>
  </div>
  
  
</div>

</template>

<script>
export default {
  props: ['error']
}
</script>