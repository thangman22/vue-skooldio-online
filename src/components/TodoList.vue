<template>
    <ul>
        <li v-for="todo in todoItems" :key="todo.time" :class="{red: !todo.completed,green: todo.completed}">
    </ul>
</template>

<script>
export default {
    name: 'TodoList',
    // props: ['todoItems']
    props: {
        todoItems: {
            type: Array,
            default: [],
        }
    }
}
</script>

<style>

</style>
