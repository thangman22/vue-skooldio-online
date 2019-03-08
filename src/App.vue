<template>
  <div id="app">
    <ul>
      <li v-for="todo in todos" :key="todo.time" v-html="todo.text">
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
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
            "text": "<strong>Learn Vue Router</strong>",
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
