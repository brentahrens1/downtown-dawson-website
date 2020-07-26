<template>
  <div id="app">
    <div id="nav">
      <nav-bar />
    </div>
    <router-view/>
    <div id="footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import Footer from './components/Footer'
export default {
  components: {
    NavBar,
    Footer
  },
  methods: {
  }
}
</script>

<style lang="scss">
  html {
    box-sizing: border-box;
  }

  *, 
  *:before, 
  *:after {
    box-sizing: inherit;
  }

  html, body {
    padding: 0;
    margin: 0;
  }


  #app {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  #footer {
    margin-top: auto;
  }

  p, li, a {
    font-family: 'Prompt', sans-serif;
  }

  h1, h2, h3, h4, h5 {
    font-family: 'Bungee', cursive;
  }

  ul {
    padding: 0;
  }

  li {
    list-style: none;
  }

  a:link, a:visited {
    text-decoration: none;
    color: #000;
  }
</style>
