<template>
  <div id="app">
    <ul>
      <li v-for="todo in todos" :key="todo.time">
        <div v-if="completed === false">{{todo.text | capitalize}}</div>
        <div v-else><img :src="srcUrl">Completed {{todo.text | capitalize}}</div>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'app',
  filters: {
    capitalize (val) {
      return val.toUpperCase()
    }
  },
  data() {
    return {
      srcUrl: 'https://via.placeholder.com/20',
      todos:[
        {
            "text": "Learn Vue.js",
            "completed": true,
            "time": 1526710200
        },
        {
            "text": "Learn VueX",
            "completed": false,
            "time": 1526710254
        },
        {
            "text": "Learn Vue Router",
            "completed": false,
            "time": 1526710407
        }
      ]
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
