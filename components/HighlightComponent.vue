<template>

<div>
  
<div  class="flex justify-between">

  <div class="bg-gray-800 w-7/12 rounded-2xl flex justify-center">
    <h1>Futured</h1>  
    <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error...</p>
    <img v-else :src=books[25].img >
    <h1> {{books[25].title}} </h1>
   
    
  
  </div>

<div class="bg-gray-200 w-4/12 h-60 flex flex-col justify-between">
      <div class="bg-gray-800 h-1/4 rounded-2xl">
        <p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error...</p>
    <h1> {{books[25].title}} </h1>
        </div>

      <div class="bg-gray-800 h-1/4 rounded-2xl">
      2
        </div>

      <div class="bg-gray-800 h-1/4 rounded-2xl">
        3
      </div>
</div>
 
</div>

</div>

</template>

<script>


  export default {
    mounted(){
 //let x = Math.floor((Math.random() * 179) + 0);
 // console.log(x)
    },
    data() {
      return {
        books: [],
      }
    },
    async fetch() {
      this.books = await fetch(
        'http://localhost:5000/books'
      ).then(res => res.json())
    }
  }


  
</script>
