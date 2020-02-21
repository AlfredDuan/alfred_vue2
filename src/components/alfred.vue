<template>
  <div>
    <h1>{{ msg }}</h1> 
    <h2>{{ con }}</h2> 
  </div>
</template>

<script>
export default {
  name: 'alfred',
  data () {
    return {
      msg: 'I am Alfred',
      con: 'I am Olivia'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  color: #42b983;
}
</style>