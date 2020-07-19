<template>
  <div>
    <h2>making api requests without nuxt</h2>


    <div class="container">
      <h4 v-for="post in posts" v-bind:key="post.id">
        {{post.title}}
      </h4>
    </div>
  </div>
</template>

<script>

import axios from 'axios'

export default {
  
  data() {
    return {
      posts: []
    }
  },

  mounted() {
    axios.get('https://jsonplaceholder.typicode.com/todos')
      .then(response => {
        console.log(response);
        this.posts = response.data;
      })
      .catch(error => {
        console.log(error);
      })
  }
}
</script>