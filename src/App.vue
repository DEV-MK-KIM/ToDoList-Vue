<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <TodoList></TodoList>
    <TodoFooter></TodoFooter>
  </div>
</template>

<script>
import TodoFooter from "./components/TodoFooter";
import TodoHeader from "./components/TodoHeader";
import TodoInput from "./components/TodoInput";
import TodoList from "./components/TodoList";

export default {

  /* Move to Vuex Store Mutations */

  // methods: {
  //   addOneItem(todoItem) {
  //     const obj = { completed: false, item: todoItem };
  //     localStorage.setItem(todoItem, JSON.stringify(obj));
  //     this.todoItems.push(obj);
  //   },
  //   removeOneItem(todoItem, index){
  //     localStorage.removeItem(todoItem.item); 
  //     this.todoItems.splice(index, 1);
  //   },
  //   toggleOneItem(todoItem){
  //     this.todoItemsp[index].competed = !this.todoItemsp[index].competed;
  //     localStorage.removeItem(todoItem.item);
  //     localStorage.setItem(todoItem.item, JSON.stringify(todoItem));
  //   },
  //   clearAllItems(){
  //     this.todoItems = [];
  //     localStorage.clear();
  //   }
  // },

  
  components: {
    TodoFooter,
    TodoHeader,
    TodoInput,
    TodoList
  }
};
</script>

<style>
body {
  text-align: center;
  background-color: #f6f6f6;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

input {
  border-style: groove;
  width: 200px;
}
button {
  border-style: groove;
}
.shadow {
  box-shadow: 5px 10px 10px rgba(0, 0, 0, 0.3);
}
</style>