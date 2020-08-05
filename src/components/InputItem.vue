<template>
    <div>
        <input type="text" v-model="text"/>
        <button @click="save()">Save</button>
    </div>
</template>

<script>
import { ref } from 'vue'
export default {
    name: 'InputItem',
    setup(_, context) {
        const text = ref(null)

        const save = () => {
            context.emit('on-save',text)
        }
        
        return {
            text, save
        }
    }
}
</script>

<style>

</style>
