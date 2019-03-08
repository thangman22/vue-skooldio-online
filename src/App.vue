<template>
  <div id="app">
    <ul>
      <li v-for="todo in todos" :key="todo.time" :class="{red: !todo.completed,green: todo.completed}" :style="{color:color}">
        {{todo.text | capitalize}}
      </li>
    </ul>
    <p>
      {{text}}
    </p>
    <input type="text" v-model="text">
  </div>
</template>

<script>

export default {
  name: 'app',
  methods: {
    save (val) {
      console.log('save')
    }
  },
  data() {
    return {
      text: '',
      color:'red',
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
.red{
  color: crimson;
}
.green {
  color:darkgreen;
}
</style>
