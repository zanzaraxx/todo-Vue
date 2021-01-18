<template>
    <li>
    <span>
    <input type="checkbox">
    {{task.title}}
    </span>
    <button class="btn" v-on:click="$emit('remove-task', task.id)">&times;</button>
    </li>
</template>

<script>
export default {
    props: {
        task: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>
    li {
        background-color: #fff;
        border-radius: 20px;
        display: flex;
        justify-content: space-between;
        padding: .3rem 1rem;
        margin-bottom: 1rem;
        width: 400px;
        height: 40px;
    }
    span {
        margin-top: 10px;
    }
    
    .btn {
        background-color: rgb(219, 34, 34);
        color: #fff;
        margin-top: 8px;
        width: 25px;
        height: 25px;
        border-radius: 35%;
        font-weight: bold;
        border: none;
    }
    .btn:hover, .btn:focus {
        outline: none;
    }
</style>