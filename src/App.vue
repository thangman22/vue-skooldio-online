<template>
  <div id="app">
    <ul>
      <li v-for="todo in todos" :key="todo.time" :class="{red: !todo.completed,green: todo.completed}" :style="{color:color}">
        {{todo.text | capitalize}}
      </li>
      <button @click="save()">Save</button>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'app',
  methods: {
    save2 () {
      this.save()
    },
    save () {
      console.log('save')
    }
  },
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
            "text": "Learn Vue Router",
            "completed": false,
            "time": 1526710407
        }
      ]
    }
  }
}
</script>

<style scoped>
.red{
  color: crimson;
}
.green {
  color:darkgreen;
}
</style>
