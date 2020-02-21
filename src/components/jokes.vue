<template>
  <div>
    <h1>jokeshub</h1>
    <input type="button" value="show me the jokes" @click ="showjokes">
    <p>
        {{ joke }}
    </p>
  </div>
</template>
<script>
export default {
  name: 'jokes',
  data () {
    return {
      joke: 'Are you ready'
    }
  },
  methods: {
    show:function(){
        alert('show is running');
    },
    showjokes:function(){
        var that = this;
        that.$axios.get("https://autumnfish.cn/api/joke").then(function(response){
          that.joke = response.data;
      },function(err){
          console.log("err");
      })
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
p {
    background-color: yellow;

}
</style>
