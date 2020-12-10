<template>
  <div id="app">
    <NavBar />
    <Header />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    Header
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap');

    $SoftBlue: hsl(231, 69%, 60%);
    $SoftRed: hsl(0, 94%, 66%);
    $DarkBlue: hsl(229, 31%, 21%);
    $LightBlue: hsl(229, 8%, 60%);

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  #app {
    font-family: 'Rubik', sans-serif;
  }
  .btn {
    text-decoration: none;
    color: #fff;
    background-color: $SoftBlue;
    padding: 10px 30px;
    border-radius: 4px;
    -webkit-box-shadow: 0px 2px 30px -8px rgba(148,148,148,1);
    box-shadow: 0px 2px 30px -8px rgba(148,148,148,1);
  }
</style>
