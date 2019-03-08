<template>
    <div>
        <input type="text" v-model="text"/>
        <button>Save</button>
    </div>
</template>

<script>
export default {
    name: 'InputItem',
    data() {
        return {
            text: null
        }
    }
}
</script>

<style>

</style>
