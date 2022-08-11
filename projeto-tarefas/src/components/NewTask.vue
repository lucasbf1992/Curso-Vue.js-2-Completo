<template>
    <div class="new-task">
        <input @keydown.enter="add" type="text" v-model="name"/>
        <button @click="add">+</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: ''
        }
    },
    methods: {
        add() {
            this.$emit('taskAdded', { name: this.name })
            this.name = ''
        }
    },

}
</script>

<style>

</style>