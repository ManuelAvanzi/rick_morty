<template>
    
    <div id="container">
        <card-box 
        v-for="personaggio in personaggi"
        :key="personaggio.id"
        :personaggio="personaggio"
        />
    </div>

</template>


<script>

import CardBox from './CardBox.vue'

export default {
    components:{
        CardBox,
    },

    props:{
         personaggi: Array
    }
}
</script>


<style lang="scss" scoped>

#container {
    margin: 0 auto;
    border:1px solid black;
    display: flex;
    width: 1000px;
    flex-wrap: wrap;
    background-color: rgba(255, 248, 220, 0.322);
    border-radius: 5px;

}
</style>