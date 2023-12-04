<script setup>
import { ref } from "vue"
const todos = ref([
    { userId: 1, id: 1, title: "Run for 3k", completed: false },
    { userId: 1, id: 1, title: "Create New Project<", completed: false },
    { userId: 1, id: 1, title: "Staff Meeting", completed: false },
    { userId: 1, id: 1, title: "Run for 2k", completed: false },
])
</script>

<template>
    <ul>
        <!-- <li><input type="checkbox">Run for 3k</li>
            <li><input type="checkbox">Staff Meeting</li>
            <li><input type="checkbox">Create New Project</li>
            <li><input type="checkbox">Run for 2k</li> -->
        <ul>
            <li v-for="todo in todos" v-bind:key="todo.id">
                <input type="checkbox" v-model="todo.completed">{{ todo.title }}({{ todo.userId }})
            </li>
        </ul>
    </ul>
</template>

<style scoped>
ul {
    margin: 0 auto;
    list-style: none;
    width: 500px;
}
</style>