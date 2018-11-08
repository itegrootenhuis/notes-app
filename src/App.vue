<template>
    <div id="app">
      <Slide>
        <div id="nav">
          <router-link to="/"><font-awesome-icon icon="js"/> Home</router-link>
          <router-link to="/settings">Setting</router-link>
        </div>
      </Slide>
      <router-view/>
    </div>  
</template>


<script>
import { Slide } from 'vue-burger-menu'
import sass from 'sass-loader'
 
export default {
    components: {
        Slide,
    }
}
</script>


<style lang="scss">
body{
  background-color: #1a1a1a
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #fff;
  display: block;
  text-decoration: none;
  &:hover{
    text-decoration: underline;
  }
}

#nav a.router-link-exact-active {
  color: #76f8f8;
}
</style>
