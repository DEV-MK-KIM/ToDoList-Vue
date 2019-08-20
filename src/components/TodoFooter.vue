<template>
  <div class="clearAllContainer">
    <span class="clearAllButton" @click="clearTodo">Clear All</span>
  </div>
</template>

<script>
export default {
    methods: {
        clearTodo(){
            localStorage.clear();
        }
    }
};
</script>

<style scoped>
.clearAllContainer {
  width: 8.5rem;
  height: 50px;
  line-height: 50px;
  background-color: white;
  border-radius: 5px;
  margin: 0 auto;
}
.clearAllButton {
  color: #e30303;
  display: block;
}
</style>
