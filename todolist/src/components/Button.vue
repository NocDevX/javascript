<template>
    <button @click="addTask()" :style="{ background: color }" class="btn">{{ title }}</button>
</template>

<script>
export default {
    name: "Button",
    props: {
        title: {
            type: String,
            default: "Button",
        },
        color: String,
    },  
    methods: {
        addTask: function () {
            console.log("Task Added!");
        },
    },
};
</script>
