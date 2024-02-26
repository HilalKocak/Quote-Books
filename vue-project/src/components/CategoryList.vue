<template>
    <div class="column">
      <h2>Categories</h2>
      <div class="category" v-for="(category, index) in categories" :key="index">
        <span class="badge">{{ category }}</span>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
    categories: Array
   },
    data() {
    
}

  }
  </script>
  
  <style scoped>
   .badge {
    display: inline-block;
    margin-right: 5px;
    margin-bottom: 5px;
    padding: 5px 10px;
    background-color: #007bff;
    color: #fff;
    border-radius: 5px;
  }
  </style>
  