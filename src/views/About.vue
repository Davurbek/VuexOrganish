<template>
  <div>
   <h3>Image</h3>
   <div class="todos">
     <div  v-for="url in allUrls" :key="url.id" class="todo"  >
       {{url.url}}
      <img :src="url.url" alt="">
       <i  class="fas fa-trash-alt"></i>
     </div>
   </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';

export default {
  computed: {
    ...mapGetters([
      'allUrls',
    ])
  },
  methods: {
    ...mapActions([
      'fetchUrls'
    ])
  },
  created () {
    this.fetchUrls();
  },
};
</script>

<style  scoped>
.todos {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 1rem;
}
.todo {
  border: 1px solid #ccc;
  background: #41b883;
  padding: 1rem;
  border-radius: 5px;
  text-align: center;
  position: relative;
  cursor: pointer;
}
img{
  width: 300px;
}
i {
  position: absolute;
  bottom: 10px;
  right: 10px;
  color: #fff;
  cursor: pointer;
}
</style>
