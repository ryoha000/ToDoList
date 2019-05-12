<template>
  <div>
    <div>ToDoList</div>
    <div>
      <label>
        Task
        <input type="text" v-model="newTodoName">
      </label>
      <button @click="addTodo">add</button>
    </div>
    <div v-for="name in Todos" :key="name.id">
      <div>Task: {{ name }}
        <button @click="Accomplishments.push(name);Todos.splice(name,1)">Accomplish!</button>
      </div>
    </div>
    <div v-for="item in Accomplishments" :key="item.id">
      <div class="item">
        <div class="name">Accomplishment: {{ item }}
          <button @click="Accomplishments.splice(name,1)">Dlete</button>
        </div>
      </div>
    </div>
    <div>
      <button @click="Todos.splice(name)">すべてのタスクを破壊して気持ちよくなるボタン</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Todos: ["物理実験計画書","読書"],
      newTodoName: "",
      
      Accomplishments: [ "書評" , "掃除" ],
      newAccomplishmentName: "",
    };
  },
  methods: {
    addTodo() {
      this.Todos.push( this.newTodoName );
    },
    Accomplish() {
      Accomplishments.push( name );
    }
  }
};
</script>

<style>
</style>