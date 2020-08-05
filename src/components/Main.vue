<template>
  <div id="app">
    <TodoList :todoItems="todosItem"></TodoList>
    <InputItem @on-save="addTodoItem"></InputItem>
  </div>
</template>

<script>
import TodoList from '@/components/TodoList'
import InputItem from '@/components/InputItem'

export default {
  name: 'main',
  components: {TodoList,InputItem},
  completed: {
    sortItem () {
      return this.todos.sort((a,b) => {b.time - a.time})
    }
  },
  methods: {
    addTodoItem (text) {
        this.todosItem.push({
            "text": text,
            "completed": false,
            "time": Date.now()
        })
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
