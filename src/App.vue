<template>
  <div id="app">
    <div id="nav">
      <nav-bar />
    </div>
    <router-view/>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
export default {
  components: {
    NavBar: NavBar
  }
}
</script>

<style lang="scss">
  html {
    box-sizing: border-box;
    font-family: 'Prompt', sans-serif;
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
