<template>
  <div>
    <h2>making api requests</h2>


    <div class="container">
      <Card v-for="post in posts" v-bind:key="post.id" :post="post"/>

      <button class="btn btn-danger" v-scroll-to="'body'">Back to Top</button>
    </div>
  </div>
</template>

<script>

import axios from 'axios'
import Card from '@/components/Card'
import {mapGetters} from 'vuex'

  export default {
    data() {
      return {
        allPosts: ''
      }
    },
    computed: {
      // posts() {
      //   return this.$store.getters.posts
      // }
      ...mapGetters(['posts']) //can access multiple getters using mapgetters
    },
    // async fetch({store}) {
    //   let {data} = await axios.get('https://jsonplaceholder.typicode.com/posts')
    //   //return allPosts()
    //   store.dispatch('setPosts', data)
    // },
    head: {
      title: 'List of Posts'
    }
  }
</script>