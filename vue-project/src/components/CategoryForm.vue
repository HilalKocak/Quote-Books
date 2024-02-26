<template>
    <div class="column">
      <h2>Add Category</h2>
      <input type="text" v-model="newCategory" placeholder="New category name">
      <button @click="addCategory">Add</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newCategory: ''
      };
    },
    methods: {
        addCategory() {
    if (this.newCategory !== '') {
      this.$emit('add-category', this.newCategory);
      this.newCategory = ''; // Clear input
    }
  }
    }
  }
  </script>
  
  <style scoped>
 
  </style>
  