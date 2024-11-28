
<template>
    <div class="toDoWrapper">

        <div class="todoHeader">
            <h2>  {{ message }} </h2>
        </div>
        <div class ="toDO">
            <form @submit.prevent="addToDo">
                <input v-model="newToDo" required 
        placeholder="new task"/>

                <button>"Add Task"</button>
            </form>

            <ul>

                <li v-for="todo in todos" :key="todo.id" >

                    {{ todo.text }}
                    <button @click="removeToDo(todo)"> X </button>
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
