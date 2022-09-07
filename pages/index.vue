<template>
        <ul> 
          <li v-for="user in users" :key="user.id">{{user.name}} </li>
        </ul> 
        
    <!-- <HighlightComponent/> -->
       
        
  
  
</template>

<script>
  
import { async } from 'q'
// import HighlightComponent from '../components/HighlightComponent.vue'
export default {
    name: "IndexPage",
    //  components: { HighlightComponent },
    async asyncData({$axios}){
      try {
        let users = await $axios.$get(
          "https://jsonplaceholder.typicode.com/users"
        );
        return {users};
      } catch(error) {
        console.log(error);
      }
    },
    data(){
      return {
        users: [],
      };

      },
    };




</script>