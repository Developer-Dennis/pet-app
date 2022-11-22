<template>
  <div class="grid">
        <div  class="col-12 md:col-6 lg:col-3" v-for="pet in pets" :key="pet.id">
            <!-- <h3>{{ pet.name }}</h3> -->
            <Pet @Remove-pet="$emit('Remove-pet', pet.id)" @add-favorite="$emit('add-favorite', 
            pet.id)" :pet="pet" />
        </div>
    </div>
</template>

<script>
import Pet from '../components/Pet.vue'
export default {
    props:{
        pets: Array
    },
    components:{
        $emits: ["Remove-pet", "add-favorite"],
        Pet
    }
}
</script>

<style>

</style>