<template>
    <div
        @dblclick="$emit('toggle-reminder', task.id)"
        :class="[task.reminder ? 'reminder' : '', 'task']"
    >
        <h4>
            {{ task.text }}
            <i @click="$emit('delete-task', task.id)" class="fas fa-times"></i>
        </h4>
        <small>{{ task.day }}</small>
    </div>
</template>

<script>
export default {
    name: "Task",
    props: {
        task: Object,
    },
};
</script>

<style scoped>
.task {
    background: #f4f4f4;
    margin: 0.3rem auto;
    padding: 1rem;
    cursor: pointer;
}

.task.reminder {
    border-left: 0.3rem solid green;
}

.task > h4 {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.fas {
    color: darkred;
}
</style>
