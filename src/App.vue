<script setup>
import PostList from './components/PostList.vue'
import NavBart from './components/NavBart.vue';
import NavFooter from './components/NavFooter.vue';
</script>

<template>
  <header>
    <NavBart/>
  </header>

  <main>
      <PostList />
  </main>

  <footer>
    <NavFooter/>
  </footer>

</template>

<style scoped>

/* header,
main,
footer {
  max-width: 1200px;
  margin: 0 auto;
} */

/* Estilos para pantallas pequeñas */
@media screen and (max-width: 768px) {
  header,
  main,
  footer {
    padding: 0 20px;
  }
}

/* Estilos para pantallas de 769px a 1024px */
@media screen and (min-width: 769px) and (max-width: 1024px) {
  header,
  main,
  footer {
    max-width: 90vw;
    padding: 0 10px;
    margin-right: 3%;
  }

  header{
    margin-right: 60%;
  }

}
</style>
