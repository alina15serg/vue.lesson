<script setup>
import{ref} from"vue";
const users =ref([
    {id:1,username:'Bret'},
    {id:2,username:'Ervin'},
    {id:3,username:'Samantha'},
])
</script>

<template>
<form action="new todo">
    <input type="text" placeholder="new todo">
    <select>

    <option value="value">select user</option>
        <option value="value">Nine</option> 
    </select>
    <button>Add ToDo</button>
</form>
</template>

<style scoped>
form {
    margin: 0 auto;
    list-style: none;
    width: 500px;
    display: flex;
    flex-direction: column;
    gap: 4px;
    margin-top: 30px;
}
</style>