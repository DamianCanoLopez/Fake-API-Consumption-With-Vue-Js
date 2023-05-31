<script>
import axios from 'axios';

export default{
  name: "PostList",

  data(){
    return{
      posts: []
    }
  },

  methods: {
    async getPosts(){
      let url = 'https://jsonplaceholder.typicode.com/posts';

      let response = await axios.get(url)
      this.posts = response.data
    },

    async postData(){
      let url = 'https://jsonplaceholder.typicode.com/posts';
      let post ={
       title: 'Helo',
       body: 'This is a method POST in axios'
     };

     axios.post(url, post)
    }
  },

   created(){

    this.getPosts();
    this.postData();

    // ejemplo de como hacer peticiones a otros metodos de la API con axios
    // let post ={
    //   title: 'Helo',
    //   body: 'This is a method POST in axios'
    // };

    // axios.post(url, post)

    // ejemplo de como hacer peticiones a otros metodos de la API
    // let texto = {name: 'Carlos'};
    // let post = {
    //   method: 'POST',
    //   body: JSON.stringify(texto),
    //   headers: {
    //     'Content-Type': 'application/json'
    //   }
    // }

    // ejemplo de como se hacen peticiones con fech
    // const response = await fetch(url);
    // if(response.ok){
    //   const postsData = await response.json()
    //   this.posts = postsData;
    // }else{
    //   alert('Error HTTP: ' + response.status)
    // }
  },
};
</script>

<template>
  <div id="container">
    <div v-for="post in posts" :key="post.id" class="cart">
      <h3>{{ post.id }}- {{ post.title }}</h3>
      <p>{{ post.body }}</p>
    </div>
  </div>
</template>

<style scoped>
#container{
  display: flex;
  flex-wrap: wrap;
  margin-top: 2%;
  margin-bottom: 2%;
}

.cart{
  width: calc(33.33% - 20px);
  margin: 10px;
  border: 1px solid #ccc;
  padding: 1%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.cart:hover{
  box-shadow: 3px 7px 10px -2px rgb(149, 50, 211);
}

/* Estilos para pantallas pequeñas */
@media screen and (max-width: 768px) {
  .cart {
    width: calc(50% - 20px);
  }
}

/* Estilos para pantallas aún más pequeñas */
@media screen and (max-width: 576px) {
  .cart {
    width: calc(100% - 20px);
  }
}

/* Estilos para pantallas de 769px a 1024px */
@media screen and (min-width: 769px) and (max-width: 1024px) {
  .cart {
    width: calc(25% - 20px);
  }
}
</style>
