<template>

 <v-container>
   <Hero />
   <v-row>
     <Project-card 
     v-for="project in projectCards"
     :key="project.id"
     :card="project"
     />
   </v-row>
   
 </v-container>
 
</template>

<script>
import {projects} from "@/assets/data.js"
export default {
  data(){
    return{
      projectCards: projects
    }
    
  }

}
</script>

<style>

</style>