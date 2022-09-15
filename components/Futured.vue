<template>
<div>

<p>Futured</p>
    <br>

<br>
<div class="test">
<p v-if="$fetchState.pending">Loading....</p>
    <p v-else-if="$fetchState.error">Error...</p>
    <img width="400" v-else :src=books[1].img >
</div>
  
<div class="flexbox-container">
    <div class="flexbox-item flexbox-item-1">  
     <h1> {{books[22].title}} </h1>
     </div>
    <div class="flexbox-item flexbox-item-2">
        <h1> {{books[24].title}} </h1>
    </div>
    <div class="flexbox-item flexbox-item-5">
        <h1> {{books[22].title}} </h1>
    </div>
    <div class="flexbox-item flexbox-item-1">
        <h1> {{books[22].title}} </h1>
    </div>
    <div class="flexbox-item flexbox-item-2">
        <h1> {{books[22].title}} </h1>
    </div>
    
</div>
</div>


</template>

<style>

.test {
    background-color: blue;
    width: auto;
    height: 0;
    
}
.flexbox-container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-end;
  

}

.flexbox-item {
width: 200px;
margin: 10px;
background-color: #424242; 
height: 90px;
border-radius: 20px;
padding: 20px;
background-color: rgb(31 41 55);;

}


</style>

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