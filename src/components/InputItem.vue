<template>
    <div>
        <input type="text" v-model="text"/>
        <button @click="save()">Save</button>
    </div>
</template>

<script>
export default {
    name: 'InputItem',
    data() {
        return {
            text: null
        }
    },
    methods: {
        save () {
            this.$emit('onSave',this.text)
        }
    }
}
</script>

<style>

</style>
