<template>
  <div id="app">
    <img src="./assets/logo.png" @click="getSeller" >
    <router-view/>
  </div>
</template>

<script>
  import VueResource from 'vue-resource'
export default {
    data(){
        return {
            seller :"23"
        }
    },
    methods:{
        getSeller(){
          this.$http.get('/api/seller').then((response) => {
            response = response.body;
            console.log(response,234)
          });
        }
    }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
