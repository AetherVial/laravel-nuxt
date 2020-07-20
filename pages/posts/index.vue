<template>
  <div>
    <h2>making api requests</h2>


    <div class="container">
      <h4 v-for="post in posts" v-bind:key="post.id">
        {{post.title}}
      </h4>
    </div>
  </div>
</template>

<script>

import axios from 'axios'

// export default {
  
//   data() {
//     return {
//       posts: []
//     }
//   },

//   mounted() {
//     axios.get('https://jsonplaceholder.typicode.com/todos')
//       .then(response => {
//         console.log(response);
//         this.posts = response.data;
//       })
//       .catch(error => {
//         console.log(error);
//       })
//   }
// }

  export default {
    data() {
      return {
        posts: '20 posts'
      }
    },
    async asyncData() {
      let res = await axios.get('https://jsonplaceholder.typicode.com/todos')
      return {posts: res.data}
    },
    head: {
      title: 'List of Posts'
    }
  }
</script>