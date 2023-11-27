<script setup>
//Импорт функции ref
import { ref } from 'vue'
//Создание реактивных переменных
let name = ref('')
let birth = ref(0)
let year = ref(0)
let spicok =ref('')

let names = ref(['Джон','Алия','Питер'])
let todos =ref([
    {status:true,name:'Убраться дома'},
    {status:false,name:'Погулять с собакой'},
    {status:false,name:'Купить продукты'},
]);

function addName(){
    names.value.push(name.value)
}
function addItem(){
    todos.value.push({status:false,name:spicok.value});
}
</script>

<template>
    <div>
        
<!--v-model привязка поля ввода к переменной-->
        <input type="text" placeholder="имя" v-model="name"/>
        <button>Добавить имя</button>
        <input type="text" placeholder="имя" v-model="spicok"/>
        <button v-on:click="addItem">Добавить список</button>
<!--{{  }}- вывод переменой в код-->
        <p>Имя:{{ name }}</p>
        <p>Возраст:{{ year-birth }}</p>
<!-- вывести список names-->
       <ul>
        <li v-for="name in names">{{ name }}</li>
       </ul>
<!--Вывести список todos, который является объектом-->
       <ul>
        <li v-for="todo in todos"><input type="checkbox" v-model="todo.stutus"><p>{{ todo.name}}</p></li>
       </ul>
    </div>
</template>

<style scoped></style>
