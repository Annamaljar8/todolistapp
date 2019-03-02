<template>
  <div id="app">
    <div class="container text-center p-5">
      <h1>{{ title }}</h1>
      <div class="row justify-content-around m-5">
        <button type="button" v-on:click="add()"  class="btn btn-primary">Add</button>
        <button type="button" v-on:click="remove()" class="btn btn-success">Remove</button>
        <button type="button" v-on:click="delite()" class="btn btn-danger">Clear</button>
      </div>
      <div class="row justify-content-center">
        <ul class="w-50">
          <li v-for="(todo, index) in todos" :key="index" class="list-group-item">
                        Task number {{ index+1 }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      title: 'To Do List',
      todos: []
    }
  },
  methods: {
       add() {
          this.todos.push(this.index);
            },
       remove() {
          this.todos.splice(this.index, 1)
            },
       delite() {
          this.todos = []
            },
        }
}
</script>

<style lang="scss">

</style>
