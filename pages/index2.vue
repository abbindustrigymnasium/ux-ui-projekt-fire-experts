<template>
  <div>
    <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error while fetching mountains</p>
    <ul v-else>
      <li v-for="(mountain, index) in mountains" :key="index">
        {{ mountain.title }}
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        mountains: []
      }
    },
     async fetch() {
      this.books = await fetch(
        'http://localhost:5000/books'
      ).then(res => res.json())
    }
  }
</script>