
<template>
    <div class="toDoWrapper">

        <div class="todoHeader">
            <h2>  {{ message }} </h2>
        </div>
        <div class ="toDO">
            <form  @submit.prevent="addToDo">
                <input class="forms" v-model="newToDo" required 
        placeholder="New task"/>

                <button class="button">Add Task</button>
            </form>

            <ul>

                <li class="forms" v-for="todo in todos" :key="todo.id" >

                    {{ todo.text }}
                    <button class="button"  @click="removeToDo(todo)"> X </button>
                </li>

            </ul>

        </div>
    </div>
</template>

<script setup>

import { ref } from 'vue';
const message = ref('Needs doing:');
let id = 0

const newToDo = ref('')
const todos = ref([
{ id: id++, text: 'Make a To Do List' }
])

function addToDo() {

    todos.value.push({ id: id++, text: newToDo.value })
        newToDo.value = ''

    newToDo.value = ''
}

function removeToDo(todo) {

todos.value = todos.value.filter((t) => t !== todo)
    
}

</script>

<style scoped>

.forms{

    height: 2.5em;
    font-family: "Lucida Console", "Courier New", monospace;
}

.button{
border-radius: 12%;
border-style: solid;
border-color: #4d7b54;
background-color: #92ca8b;
color: #395a3e;
height: 2em;
margin-left: 1em;
font-family: "Lucida Console", "Courier New", monospace;
}

.toDoWrapper{

    margin-top: 5em;
}

</style>
