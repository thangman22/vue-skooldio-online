<template>
    <ul>
        <li v-for="todo in todoItems" :key="todo.time" :class="{red: !todo.completed,green: todo.completed}">{{todo.text}}</li>
    </ul>
</template>

<script>
export default {
    name: 'TodoList',
    props: {
        todoItems: {
            type: Array,
            default: () => []
        }
    }
}
</script>

<style>

</style>
