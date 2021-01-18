<template>
    <div class="container">
        <firstTable />
        <secondTable :taskData="taskData" v-on:remove-task="removeTask" @add-task="newTask"/>
        <thirdTable />
    </div>
</template>

<script>
import firstTable from './firstTable.vue';
import secondTable from './secondTable.vue';
import thirdTable from './thirdTable.vue';

export default {
    components: {
        firstTable,
        secondTable,
        thirdTable,
    },
    data() {
        return {
            taskData: [
                {id: 1, title: 'sbgsdjfb', completed: false}
            ]
        }
    },
    methods: {
        removeTask(id) {
            this.taskData = this.taskData.filter(t => t.id !== id)
        },
        newTask(task) {
            this.taskData.push(task)
        }
    }
};
</script>

<style scoped>

    div {
        display: inline-block;
    }

    .container {
        margin-right: 30px;
        margin-left: 30px;
        height: 100%;
        width: 100%;
    }

</style>