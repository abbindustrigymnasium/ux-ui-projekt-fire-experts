<template>
<div class="bg-gray-800 w-7/12 rounded-2xl flex justify-center">
    <ul>
        <li v-for="(book, index) in books" :key="index">
            {{ book.books }}
        </li>
    </ul>
</div>
</template>

<script>
  export default {
    data() {
      return {
        books: []
        
      }
    },
    async fetch() {
      this.books = await fetch(
        'http://localhost:5000/books'
      ).then(res => res.json())
    }
  }
</script>
