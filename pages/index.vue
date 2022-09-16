<template>
  <div>
    <!-- <HighlightComponent/> -->
    <Futured/>
    <!-- <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error...</p>
    <ul v-else>
      <li v-for="(book, index) in books" :key="index">
        {{ book.title }}
      </li>
    </ul> -->
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
        'https://api.nuxtjs.dev/books'
      ).then(res => res.json())
    }
  }
</script>