
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

<template>
    <div class="column">
      <h2>Add Category</h2>
      <input type="text" v-model="newCategory" placeholder="New category name">
      <button @click="addCategory">Add</button>
    </div>
  </template>
  
  
  <style scoped>
  .column {
    max-width: 400px;
    margin: 20px auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  h2 {
    color: #34495e;
    font-size: 22px;
    text-align: center;
    margin-bottom: 20px;
  }
  
  input[type="text"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 20px;
    border: 1px solid #bdc3c7;
    border-radius: 4px;
    box-sizing: border-box;
  }
  
  button {
    width: 100%;
    padding: 10px;
    background-color: #27ae60;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  button:hover {
    background-color: #229954;
  }
  </style>
  