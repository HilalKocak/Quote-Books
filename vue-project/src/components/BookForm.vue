<template>
    <div class="column">
      <h2>Kitap Ekle</h2>
      <input type="text" v-model="newBook.author" placeholder="Author">
      <input type="text" v-model="newBook.title" placeholder="Book">
      <select v-model="newBook.category">
        <option disabled value="">Category</option>
        <option v-for="(category, index) in categories" :key="index">{{ category }}</option>
      </select>
      <button @click="addBook">Add</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newBook: { author: '', title: '', category: '' },
      };
    },
    methods: {
      addBook() {
       
        if (this.newBook.author !== '' && this.newBook.title !== '' && this.newBook.category !== '') {
          this.books.push({ ...this.newBook });
          this.newBook = { author: '', title: '', category: '' }; // Clear form
        }
      }
    }
  }
  </script>
  
  <style scoped>
 
  </style>
  