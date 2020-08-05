<template>
    <div class="alert">
        <slot name="header"></slot>
        <slot name="text"></slot>
    </div>
</template>

<script>
export default {
    name: 'Alert'
}
</script>

<style>
    .alert{
        border: 1px solid crimson;
        padding: 10px;
    }
</style>
