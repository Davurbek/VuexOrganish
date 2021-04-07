<template>
  <div class="home">
    <div class="container">
        <AddTodos></AddTodos>
        <FilterTodos></FilterTodos>
        <Todos></Todos>
      
    </div>
 
  </div>
</template>

<script>
/* eslint-disable */
import Todos from "@/components/Todos.vue";
import AddTodos from '@/components/AddTodos.vue';
import FilterTodos from '@/components/FilterTodos.vue';
export default {
  name: "Home",
  components: {
    Todos,
    AddTodos,
    FilterTodos
  },
};
</script>

<style scoped>
.container {
  max-width: 1100px;
  margin: auto;
  overflow: auto;
  padding: 0 2rem;
}
</style>
