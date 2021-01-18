<template>
    <div>
        <p class="nameTable">Мои задачи</p>
        <ul>
            <taskItem v-for="task in taskData" 
            :key="task.id" 
            :task="task"
            v-on:remove-task="removeTask"
            />
        </ul>
        <addTask @add-task="newTask"/>
    </div>
</template>

<script>
import taskItem from './taskItem.vue';
import addTask from './addTask.vue';

export default {
    components: {
        taskItem,
        addTask,
    },
    props: ['taskData'],
    methods: {
        removeTask(id) {
        this.$emit('remove-task', id);
        },
        newTask(task) {
            this.taskData.push(task)
        }
    }
}
</script>

<style scoped>
    div {
        height: 100%;
        width: 33%;
    }

    .nameTable {
        font-weight: bold;
        font-size: 18pt;
    }
    ul {
        list-style-type: none;
        margin: 0px;
        padding: 0px;
    }
</style>