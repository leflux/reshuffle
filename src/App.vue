<template>
  <div id="app">
    <!-- feature section -->
    <section class="feature" :style="{ backgroundImage: 'url(' + require(`@/assets/${feature.image}`) + ')' }">
      <div class="info">
        <h1>{{ feature.title }}</h1>
        <div class="description">
          <p>{{ feature.description }}</p>
          <p>Starring {{ feature.starring.join(', ') }}</p>
          <p>Genre: {{ feature.genre.join(', ') }}</p>
        </div>
      </div>
    </section>
    <!-- action bar with shuffle and search -->
    <section class="action">
      <div class="shuffle">
        <button>Shuffle</button>
      </div>
      <div class="search">
        <input type="text" placeholder="Search" />
      </div>
    </section>
    <!-- result section -->
    <section class="result">
      <div class="item" v-for="(item, i) in result" :key="i" :style="{ backgroundImage: 'url(' + require(`@/assets/${item.image}`) + ')' }">
        <div class="info">
          <h2>{{ item.title }}</h2>
          <div class="description">
            <p>{{ item.description }}</p>
            <p>Starring {{ item.starring.join(', ') }}</p>
            <p>Genre: {{ item.genre.join(', ') }}</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data () {
    return {
      feature: {
        title: 'The Yellow Storm',
        description: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.',
        starring: ['Will Smith', 'Arnold Schwarzenegger', 'Denzel Washington'],
        genre: ['Action', 'Thriller'],
        image: 'example-title.jpg'
      },
      result: [
        {
          title: 'Lorem Ipsum',
          description: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat',
          starring: ['Random Girl', 'Shuffle Dude'],
          genre: ['Mystery', 'Horror'],
          image: 'preview1.jpg',
        }, 
        {
          title: 'Lorem Ipsum',
          description: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat',
          starring: ['Random Girl', 'Shuffle Dude'],
          genre: ['Romantic', 'Family'],
          image: 'preview2.jpg',
        }, 
        {
          title: 'Lorem Ipsum',
          description: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat',
          starring: ['Random Girl', 'Shuffle Dude'],
          genre: ['Action', 'Thriller'],
          image: 'preview3.jpg',
        }
      ]
    }
  }
}
</script>

<style>
/* general */
body, html {
  --c-text-normal: #7e8a9a;
  --c-text-light: #eee;
  --c-background: #282c31;
  --c-background-element: #394047;
  --c-background-element-variant: #57606b;
  --c-accent: #9aeab9;
  --c-accent-variant: #78d19a;
  --c-shadow: #0e1013;
  background-color: black; 
  color: var(--c-text-normal);
  padding: 0;
  margin: 0;
}
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* feature section */
.feature {
  background-size: cover;
  background-position: center center;
  height: 50vh;
}
.feature h1 {
  font-size: 3em;
  margin: 0 0 .5em 0;
}
.feature .info {
  width: 75vw;
  height: inherit;
  padding: 15vh 42vw 2em 4em;
  box-sizing: border-box;
  background: linear-gradient(to right, rgba(0,0,0,1), rgba(0,0,0,0));
  color: white;
}
/* action section */
.action {
  background: var(--c-background);
  height: 15vh;
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: center;
}
.action .shuffle button,
.action .search input {
  border: none;
  outline: none;
  font-size: 1.5em;
  color: var(--c-text-normal);
  background: var(--c-background-element);
  box-shadow: 0 8px 20px -8px var(--c-shadow);
  transition: all 0.2s;
}
.action .shuffle button {
  margin-right: 10px;
  padding: 1em 1.5em;
}
.action .search input {
  width: 25vw;
  padding: 1em;
}
.action .search input::placeholder {
  color: var(--c-text-normal);
}
/* result section */
.result {
  height: 35vh;
  display: flex;
  flex-flow: row nowrap;
  align-items: stretch;
}
.result .item {
  flex-grow: 1;
  background-size: cover;
  background-position: center center;
}
.result .item h2 {
  font-size: 2em;
  margin: 0 0 .5em 0;
}
.result .item .info {
  width: 75%;
  height: 35vh;
  padding: 3em 15% 2em 4em;
  box-sizing: border-box;
  background: linear-gradient(to right, rgba(0,0,0,1), rgba(0,0,0,0));
  color: white;
}

</style>
