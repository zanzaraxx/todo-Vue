<template>
    <form @submit.prevent="onSubmit">
        <input class="txt" type="text" placeholder="Введите новую задачу" v-model="title">
        <button class="btn" type="subimt">+</button>
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
                this.title = ''
                
            }
        }
    }
}
</script>

<style scoped>

    form {
        background-color: #fff;
        border-radius: 20px;
        display: flex;
        justify-content: space-between;
        padding: .3rem 1rem;
        margin-bottom: 1rem;
        margin-top: 40px;
        width: 400px;
        height: 40px;
    }

    .txt {
        width: 360px;
        font-size: 16pt;
        border: none;
    }

    .txt:hover, .txt:focus {
        outline: none;
    }

    .btn {
        background-color: #63c57a;
        font-size: 40pt;
        padding: 0px;
        color: #fff;
        font-weight: bold;
        margin-top: -30px;
        margin-right: -30px;
        height: 100px;
        width: 100px;
        border-radius: 50%;
        border: none;
    }
    .btn:hover, .btn:focus {
        outline: none;
    }

</style>