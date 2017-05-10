<template>
  <div id="app">
    <div class='navigation'>
        <div class='home'> Home </div>
        <div class='links'>
          <div class='signup'> Sign Up </div>
          <div class='login'> Login </div>
        </div>
    </div>


    <div class='container'>
    
        <div class='boxes'>
          <div class='box'> Leads </div>
          <div class='box'> Schedule </div>
          <div class='box'> Progress </div>
          <div class='box'> Done </div>
        </div>
    </div>
    
    
  

    <img src="./assets/logo.png">
    <h1></h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100%;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
.navigation {
  border: 1px solid #fff;
  width: 100%;
  display: flex;
  justify-content: space-around;
  background-color: #5995DA;
  padding: 20px 0;
  color: #fff;
  align: center;

}
.links {
  display: flex;
  justify-content: flex-end;

}


.login {
  margin-left: 20px;
}

.container {
  display: flex;
  width: 100%;
  background-color: #D6E9FE;
  padding: 20px 0;
  align: center;

  

  
}
.boxes {
  display: flex;
  width:  100%;
  justify-content: space-around;
  padding: 20px;
  border: 1px solid ;
  align: center;
  margin: 0 auto;

}

.box {
  padding: 20px;
  display: flex;
  border: 1px solid;
  width: 20%;
  height: 500px
  
}
</style>
