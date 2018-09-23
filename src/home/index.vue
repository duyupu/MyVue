<template>
  <div id="app2">
   home index
   <input type='button' v-on:click='getPost' value='postTest'/>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods:{
   getPost:function (){

this.$http.get('http://localhost:50087/home/api').then((res)=>{
alert(res.data.Name);
console.log(res.data);
console.log(res.data.name);
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
