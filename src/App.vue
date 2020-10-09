<template>
  <div id="app">
    <img alt="Polibot" src="./assets/polibot.png" id="polibot">
    <h1>polibot keeps it wavy.</h1>
    <i>~ y o u ~ k n o w ~ t h e ~ v i b e s ~</i>
    <Main/>
    <Soundboard/>
    <Footer/>
  </div>
</template>

<script>
import Main from './components/Main.vue'
import Soundboard from './components/Soundboard.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Main,
    Soundboard,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Open Sans, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 1em;
  min-height: 100vh;
  position: relative;
  min-height: 100vh;
}
#polibot {
  max-width: 40%;
  margin: auto;
  display: inline-block;
  animation: rotation 1.2s infinite ease;
  transform: rotate(-15deg);
}
h1 {
  font-weight: 800;
}
i {
  font-weight: 400;
}
@keyframes rotation {
  50% {
    transform: rotate(15deg);
  }
}
</style>
