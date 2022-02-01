<template>
    

      <div class="card">
        <img :src="personaggio.image" class="card-image"/>
        <h3>{{personaggio.name}}</h3>

        <hr>

        <h3>{{personaggio.origin}}</h3>
        <h3>{{personaggio.species}}</h3>
      </div>

   
</template>


<script>
export default {
  props:{
    personaggio: Object
  }
}
</script>



<style lang="scss" scoped>
.card{
  width: calc(100% / 4);
  padding:20px;
  cursor: pointer;
  text-align: center;
  box-shadow: 0 0 3px grey;

   .card-image{
     width: 200px;
     border-radius: 50%;
     overflow: hidden;
   }
}
</style>