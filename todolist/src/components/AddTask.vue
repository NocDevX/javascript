<template>
    <form class="add-form">
        <div class="form-control">
            <label for="task">Task</label>
            <input type="text" name="task" placeholder="Add Task" />
        </div>

        <div class="form-control">
            <label for="date">Date & Time</label>
            <input type="text" name="date" placeholder="Add Date & Time" />
        </div>

        <div class="form-control form-control-check">
            <label for="reminder"
                >Set Reminder
                <input type="checkbox" name="reminder" />
                <p class="checkmark"></p>
            </label>
        </div>

        <input type="submit" name="saveTask" value="Save Task" class="btn btn-block" />
    </form>
</template>

<script>
export default {
    name: "AddTask",
};
</script>

<style scoped>
.add-form {
    margin-bottom: 2rem;
}

.form-control {
    margin: 0.6rem 0;
    display: flex;
    flex-direction: column;
}

.form-control label {
    display: block;
}

.form-control input {
    display: block;
    padding: 0.6rem;
    border-radius: 0.3rem;
    border: 0.15rem solid #efefef;
}

.form-control-check {
    position: relative;
    display: flex;
}

[type="checkbox"] {
    position: absolute;
    opacity: 0;
    cursor: pointer;
    right: 0;
    top: 0;
    z-index: 1;
    height: 1.8rem;
    width: 1.8rem;
}

.checkmark {
    position: absolute;
    right: 0;
    top: 0;
    height: 1.8rem;
    width: 1.8rem;
    cursor: pointer;
    background-color: #efefef;
    border-radius: .2rem;
}

.form-control-check:hover .checkmark {
    background-color: #ccc;
    transition: 0.2s;
}

.form-control-check input:checked ~ .checkmark {
    background-color: #2196F3;
}

.checkmark:after {
    content: "";
    position: absolute;
    display: none;
}

.form-control-check input:checked ~ .checkmark:after {
    display: block;
}

.form-control-check .checkmark:after {
    content: 'X';
    top: 0;
    right: 8.5px;
    color: white;
    font-size: 1.2rem;
}
</style>
