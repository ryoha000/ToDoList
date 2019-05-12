<template>
  <div>
    <div>ToDoList</div>
    <div v-for="name in Todos" :key="name.id">
      <div class="item">
        <div class="name">やったこと {{ name }}</div>
      </div>
    </div>
    <div v-for="item in Accomplishments" :key="item.id">
      <div class="item">
        <div class="name">やったこと {{ item }}</div>
      </div>
    </div>
    <div>
      <label>
        やること
        <input type="text" v-model="newTodoName">
      </label>
      <button @click="addTodo">add</button>
    </div>
    <div>
      <label>
        やったこと
        <input type="text" v-model="newAccomplishmentName">
      </label>
      <button @click="addAccomplishment">add</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Todos: ["物理実験計画書","読書"],
      newTodoName: "",
    };
  },
  data() {
    return {
      Accomplishments: [ "書評" , "掃除" ],
      newAccomplishmentName: "",
    };
  },
  methods: {
    addTodo() {
      this.Todos.push( this.newTodoName );
    }
  },
  methods: {
    addAccomplishment() {
      this.Accomplishments.push( this.newAccomplishmentName );
    }
  }
};
</script>

<style>
</style>