<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Myheader mytitle="Make your Trip" 
      aboutpage ="Shyam sunder Reddy" />
    
    
    
    <Tourbox :tours = "tours"/>
    <About aboutme="About Shyam" />
    
    
    



  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Myheader from './components/Myheader.vue'

// ----import Bookbox from './components/Bookbox.vue'

import Tourbox from './components/Tourbox.vue'
import About from './components/About.vue'


// data url: http://localhost:5555/books , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component 
    Myheader,
    
    
    Tourbox,
    About,
},

  data(){
    return {
      tours: []
    }
  },
  methods: {
    // promises

      async fetchTours(){
        const res= await fetch('https://shyamreddy.herokuapp.com/db.json')
         const data= await res.json()
          console.log(data)
         return data
      }

  },

  async created(){
    this.tours = await this.fetchTours()
  }
}
</script>










<style>




@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #304D6D;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: #A7CCED;
}

div{
  margin-bottom: 0.5em;
}



</style>


