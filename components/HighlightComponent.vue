<template>
<div>

 <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error...</p>
    <ul v-else>
      <li v-for="(book, index) in books" :key="index">
        <img :src=book.img>
      </li>
    </ul>


<div  class="flex justify-between">

  <div class="bg-gray-800 w-7/12 rounded-2xl flex justify-center">
   <div>HEJ</div> 
  
  
  </div>

<div class="bg-gray-200 w-4/12 h-60 flex flex-col justify-between">
      <div class="bg-gray-800 h-1/4 rounded-2xl">

        </div>

      <div class="bg-gray-800 h-1/4 rounded-2xl">
      
        </div>

      <div class="bg-gray-800 h-1/4 rounded-2xl">

      </div>
</div>
 
</div>

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
