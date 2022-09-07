<template>
  <div>
    <!-- <div>
      <p>{{ book.title }} av {{ book.author }}</p>
    </div> -->
    <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error while fetching books</p>
    <ul v-else>
      <li></li>
      <li v-for="(book, index) in books" :key="index">
        {{ book.title }} || {{ book.id }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      books: []
    }
  },
  async fetch () {
    this.books = await fetch(
      'http://localhost:5000/books'
    ).then(res => res.json())
  }
}
</script>