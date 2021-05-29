<template>
  <div id="app">
    <div class="login-container min-vh-100 text-center m-0 d-flex flex-column justify-content-center">
           <Login/>
    </div>
  </div>
</template>

<script>
import Login from './views/Login'
import './app.css'

export default {
  name: 'App',
  components: {Login
  },
   data() {
    return {
    }
  },
   created() {
    this.min = 0
    this.max = 250
    this.bgStyle = {
     backgroundColor: 'blue',
     boxShadow: 'inset 0.5px 0.5px 3px 1px rgba(0,0,0,.36)'
    }
    this.tooltipStyle = {
      backgroundColor: 'red',
      borderColor: '#666'
    }
    this.processStyle = {
      backgroundColor: 'green'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
</style>
