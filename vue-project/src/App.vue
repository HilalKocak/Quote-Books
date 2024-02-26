<script>
import CategoryForm from './components/CategoryForm.vue';
import BookForm from './components/BookForm.vue';
import CategoryList from './components/CategoryList.vue';
import BookTable from './components/BookTable.vue';

export default {
  data() {
    return {
      categories: ['Novel', 'Science Fiction', 'Detective', 'Fantasy'],
      books: []
    }
  },
  components: {
    CategoryForm,
    BookForm,
    CategoryList,
    BookTable
  },
  methods: {
    addCategory(category) {
      if (category && !this.categories.includes(category)) {
        this.categories.push(category);
      }
    },
    addBook(book) {
      if (book && book.title && book.author && book.category) {
        this.books.push(book);
      }
    }
  }
}
</script>

<template>
  <div id="app">
  <div class="container">
      <div class="col-6 px-3">
      <CategoryForm @add-category="addCategory" />
    </div>
    <div class="col-6 px-3">
      <BookForm @add-book="addBook" :categories="categories" />
    </div>
   
  </div>

  <div class="container">
    <div class="row">
      <div class="col px-1">
        <CategoryList :categories="categories" />
      </div>
      <div class="col books px-1">
        <BookTable :books="books" />
      </div>
    </div>
  </div>
    
   
  </div>
</template>

<style>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center; 
  
}

.col-6 {
  flex: 0 0 300px; 
  max-width: 300px; 
}

.col{
  flex: 0 0 800px; 
  max-width: 800px; 
}

.column {
  margin-left: 20px;
  padding-left: 20px;
  padding: 20px;
  margin-bottom: 20px; 
}

.books {

padding-bottom: 200px;
}

</style>
