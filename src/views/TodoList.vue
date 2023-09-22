<template>
    <div>
      <h1>Lista de tareas</h1>
      <form @submit.prevent="addTodo()">
        <input v-model="todo">
      </form>
      <el-row :gutter="12">
        <el-col :span="12" v-for="(todo, index) in todos" :key="index">
          <el-card class="box-card" shadow="hover" style="margin: 5px 0;">
            {{ todo }}
            <button @click="removeTodo(index)" type="success" icon="el-icon-check" circle></button>
          </el-card>
        </el-col>
      </el-row>
    </div>
  </template>
  
  <script>
  export default {
    name: 'TodoList',
    data() {
      return {
        todo: '',
        todos: [],
      };
    },
    methods: {
      addTodo() {
        this.todos.push(this.todo);
        this.todo = '';
      },
      removeTodo(index) {
        this.todos.splice(index, 1);
      },
    },
  };
  </script>
  
  <style>
  /* Agrega estilos específicos para esta página si es necesario */
  </style>
  