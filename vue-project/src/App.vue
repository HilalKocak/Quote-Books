<script>
import CategoryForm from './components/CategoryForm.vue';
import BookForm from './components/BookForm.vue';
import CategoryList from './components/CategoryList.vue';
import BookTable from './components/BookTable.vue';

export default {
  components: {
    CategoryForm,
    BookForm,
    CategoryList,
    BookTable
  }
}
</script>

<template>
  <div id="app">
  <div class="container">
    <div class="row">
      <div class="col-6">
        <CategoryForm />
      </div>
      <div class="col-6">
        <BookForm />
      </div>
    </div>

    <div class="row">
      <div class="col">
        <CategoryList />
      </div>
      <div class="col">
        <BookTable />
      </div>
    </div>
    
   
  </div>
    
   
  </div>
</template>


<style>

</style>
