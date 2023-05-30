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
}

.cart{
  width: calc(33.33% - 20px);
  margin: 10px;
  border: 1px solid #ccc;
  padding: 1%;
}
</style>
