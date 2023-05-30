<script setup>
import PostList from './components/PostList.vue'
import NavBart from './components/NavBart.vue';
</script>

<template>
  <header>
    <NavBart/>
  </header>

  <main>
      <PostList />
  </main>

</template>

<style scoped>



@media (min-width: 1024px) {
  /* header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  } */


  /* header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } */
}
</style>
