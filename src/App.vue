<template>
  <!-- <AppMain /> -->

  <header class="d-flex align-items-center p-4">
    <h1>Vite Boolfolio</h1>
    <nav class="d-flex gap-3 ms-auto">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/portfolio">Portfolio</RouterLink>
      <RouterLink to="/contact">Contatti</RouterLink>
    </nav>
  </header>

  <main>
    <RouterView />
  </main>


</template>



<script>
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppMain,

  },
}
</script>


<style lang="scss">

@use "./style/general.scss";

</style>
