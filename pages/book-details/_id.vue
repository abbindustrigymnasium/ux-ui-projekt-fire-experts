<template>
  <div class="bg-gray-600 rounded-3xl p-10">
    <div>
      <h1>{{ currentBook.title }}</h1>
    </div>
    <div class="mb-10">
      <p>{{ bookId }}</p>
      <p>{{ currentBook.title }}</p>
      <img :src="currentBook.img" />
    </div>
    <!-- <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error while fetching books</p>
    <ul v-else>
      <li></li>
      <li v-for="(book, index) in books" :key="index">
        {{ book.title }} || {{ book.id }}
      </li>
    </ul> -->
  </div>
</template>

<script>
export default {
  mounted () {
    console.log(this.$route.params.id)
  },
  data () {
    return {
      // books: [],
      bookId: this.$route.params.id,
      currentBook: [],
    }
  },
  async fetch () {
    // this.books = await fetch(
    //   'http://localhost:5000/books'
    // ).then(res => res.json()),
    this.currentBook = await fetch(
      'http://localhost:5000/books/' + this.$route.params.id
    ).then(res => res.json())
  }
}
</script>