<script setup>
// import { ref } from 'vue'

// let todos = ref([
//     { status: true, name: 'Run for 3k' },
//     { status: false, name: 'Staff Meeting' },
//     { status: false, name: 'Creat New Project' },
//     { status: false, name: 'Run for 2k' }
// ]);

</script>


<template>
    <div>

        <header>
            <p>ToDo List</p>
        </header>
        <!-- <button v-on:click="todo">new todo</button>
        <button v-on:click="todo">select user</button> -->
    </div>
</template>

<style scoped>
header {
    display: flex;
    padding: 20px;
    background: url('@/assets/header.svg');
    justify-content: space-between;
}

.menu {
    list-style: none;
    display: flex;
    gap: 14px;
    background: url();
}

.li {
    color: #00386B;
    text-align: center;
    font-family: Abhaya Libre ExtraBold;
    font-size: 64px;

}

.icon {
    border-radius: 26px;
    border: 1px solid #2D7DC6;
    background: #F1F1F1;
}

</style>
