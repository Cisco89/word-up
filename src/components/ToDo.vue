<template>
    <div>
        <h1 class="tittle">Todo List</h1>
        <input type="text" v-model='inputedTodo'/>
        <button v-on:click="addTodo">Add todo</button>

        <ul>
            <li class="todo" v-for="(todo, index) in todos" :key="index">
            <input type="checkbox" 
            v-model="todo.done"/>
            {{ todo.name }} 
            <button @click='removeTodo(index)'>Remove</button>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "ToDo",
    data() {
        return {
            inputedTodo: '',
            todos: []
        }
    },
    methods: {
        addTodo() {
            this.todos.push( {name:this.inputedTodo, done: false})
            this.inputedTodo = ''
        },
        removeTodo(index) {
            this.todos.splice(index, 1)
        }
    }
};
</script>

<style scope>
.todo {
    text-align: left;
}

</style>