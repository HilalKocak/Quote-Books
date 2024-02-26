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
    <div class="row">
      <div class="col-6">
        <CategoryForm @add-category="addCategory" />
      </div>
      <div class="col-6">
        <BookForm @add-book="addBook" :categories="categories" />
      </div>
    </div>

    <div class="row">
      <div class="col-3">
        <CategoryList :categories="categories" />
      </div>
      <div class="col-9">
        <BookTable :books="books" />
      </div>
    </div>
    
   
  </div>
    
   
  </div>
</template>


<style>

</style>
