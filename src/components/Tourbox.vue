<template>
    
    <div class="loc">
        
        <div v-for="tour in tours" :key="tour.id" >
            <Tour :tour="tour"/>
     
               
                
                
        
        </div>
       
    </div>

</template>

<script>

import Tour from './Tour.vue'
export default{

    name: 'Tourbox',
    components: {
        Tour
    },
    props: {
        tours: Array
    }
}

</script>

<style scoped>

.loc{

    background-color:#14213d;
    padding: 1em;
    color: rgb(243, 129, 227);
}

</style>
