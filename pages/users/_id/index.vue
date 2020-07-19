<template>
  <div>
    <h2>this is user {{$route.params.id}}</h2>
  </div>
</template>

<script>
export default {
  validate({params}) { //destructured context to use params. usually would use context :)
    return /^\d+$/.test(params.id)  //regex forcing one or more digits 
  }
}
</script>