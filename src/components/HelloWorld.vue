<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
   
    <form @submit.prevent="onSubmit">
        <label>
            New Task:
            <input type="text" name="todo" />
        </label>
        <button v-on:click="addToDo">Add To Do</button>
    </form>

    <hr />

    <ul>
        <li v-for="toDo in toDos">{{ toDo }}</li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
