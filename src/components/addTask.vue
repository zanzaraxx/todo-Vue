<template>
    <form @submit.prevent="onSubmit">
        <input type="text" v-model="title">
        <button type="subimt">Твоя новая Хуйня</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            title: ''
        }
    },
    methods: {
        onSubmit(){
            if (this.title.trim()) {
                const newTask = {
                    id: Date.now(),
                    title: this.title,
                    completed: false
                }
                this.$emit('add-task', newTask)
                
            }
        }
    }
}
</script>

<style scoped>

</style>