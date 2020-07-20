<template>
    <div class="card bg-light mb-3" style="max-width: 18 rem;">
      <div class="card-header">{{post.id}}</div>
      <h5 class="card-title">
        <nuxt-link :to='{name: "posts-id", params: {id: post.id}}'>{{post.title}}</nuxt-link>
      </h5>
      <p class="card-text">
        lorem ipsum bullshit
      </p>
    </div>
</template>

<script>
export default {
  props: {
    post: Object
  }
}
</script>