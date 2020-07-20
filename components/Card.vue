<template>
  <div>
    <div class="card bg-light mb-3" style="max-width: 18 rem;">
      <div class="card-header">{{post.id}}</div>
      <h5 class="card-title">{{post.title}}</h5>
      <p class="card-text">
        lorem ipsum bullshit
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: Object
  }
}
</script>