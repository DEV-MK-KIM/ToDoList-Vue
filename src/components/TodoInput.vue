<template>
  <div class="inputBox shadow">
    <input type="text" v-model="newTodoItem" @keydown.enter="addTodo" />
    <span class="addContainer">
      <i class="fas fa-plus addBtn" @click="addTodo"></i>
    </span>

    <Modal v-if="showModal" @close="showModal = false" >
      <!--
      you can use custom content here to overwrite
      default content
      -->
      <h3 slot="header">Hey,</h3>
      <h4 slot="body">Pleaes type and hit enter</h4>
      <h1 slot="footer">
        <i class="closeModalBtn far fa-check-square" @click="showModal = false"
        ></i>
      </h1>
    </Modal>
  </div>
</template>

<script>
import Modal from "./common/Modal";
export default {
  data() {
    return {
      newTodoItem: "",
      showModal: false
    };
  },
  methods: {
    addTodo() {
      if (this.newTodoItem !== "") {
        this.$store.commit('addOneItem', this.newTodoItem);
        this.clearInput();
      } else {
        this.showModal = true;
      }
    },
    clearInput() {
      this.newTodoItem = "";
    }
  },
  components: {
    Modal
  }
};
</script>

<style scoped>
input:focus {
  outline: none;
}
.inputBox {
  background: white;
  height: 50px;
  line-height: 50px;
  border-radius: 5px;
}
.inputBox input {
  border-style: none;
  font-size: 0.9rem;
}
.addContainer {
  float: right;
  background: linear-gradient(to right, #6478fb, #8763fb);
  display: block;
  width: 3rem;
  border-radius: 0 5px 5px 0;
}
.addBtn {
  color: white;
  vertical-align: middle;
}
.closeModalBtn {
  color: #43b983;
}
</style>
