<template>
  <div id="app">

  </div>
</template>

<script>
import TodoList from '@/components/TodoList'

export default {
  name: 'main',
  components: {TodoList},
  completed: {
    sortItem () {
      return this.todos.sort((a,b) => {b.time - a.time})
    }
  },
  data() {
    return {
      todosItem:[
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
