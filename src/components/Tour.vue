<template>
   
    <div>
       <h2>{{tour.location}}</h2>
       <h4>{{tour.place}}</h4>
       <h4>{{tour.type}}</h4>
       <h4>{{tour.cost}}</h4>
       <h4>{{tour.timeduration}} </h4>
    </div>
   
   
   
</template>

<script>

export default{
    name: 'Tour',
    props:{
       tour : Array
    }
   
}
</script>

<style scoped>

h4{
    margin: 2px;
}


div{
    background-color: #63ADF2;
    color: #003566;
    padding: 1em;
}



</style>