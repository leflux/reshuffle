<template>
  <div id="app">
    <section class="feature">
      <div class="info">
        <h1>The Yellow Storm</h1>
        <div class="description">
          <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.</p>  
          <p>Starring Will Smith, Arnold Schwarzenegger, Denzel Washington</p>
          <p>Genre: Action, Thriller</p>
        </div>
      </div>
    </section>
    <section class="action"></section>
    <section class="result"></section>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
body, html {
  padding: 0;
  margin: 0;
}
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.feature {
  background: url('./assets/example-title.jpg');
  background-size: cover;
  background-position: center center;
  height: 50vh;
}
.feature h1 {
  font-size: 3em;
  margin: 0 0 .5em 0;
}
.feature .info {
  width: 60vw;
  height: inherit;
  padding: 15vh 27vh 2em 2em;
  box-sizing: border-box;
  background: linear-gradient(to right, rgba(0,0,0,1) 10%, rgba(0,0,0,0));
  color: white;
}
.action {
  background: black;
  height: 15vh;
}
.result {
  height: 35vh;
}

</style>
