<template>
  <!-- <div class="home"></div> -->
  <AddPet  @add-pet="AddPet"/>
  <Pets @Remove-pet="Removepet" @add-favorite="addFavorite"  :pets="pets" />
</template>

<script>
import Pets from '../components/Pets.vue'
import AddPet from '../components/addPet.vue';
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    AddPet,
    Pets
  },
  data(){
    return{
      pets:[], 
  }
  },
  methods:{
    AddPet(pet){
        this.pets = [...this.pets, pet]
    },
    Removepet(id){
      // console.log("home",id)
      if(confirm("Are You Sure You Want To Remove This Pet?")){
        this.pets = this.pets.filter((pet) => pet.id !== id)
      }
    },
    addFavorite(id){
    // console.log("Home favorite", id)
    this.pets= this.pets.map((pet) => pet.id === id ? {...pet, isFavorite: !pet.isFavorite} :pet)
  },
  },
  created(){
    this.pets = [
    {
          id:1,
          name: "Ruby",
          age:2,
          url: "https://www.boredpanda.com/blog/wp-content/uploads/2021/03/url-1.jpg",
          isFavorite: false,
        },
        {
          id:2,
          name: "CoCo",
          age:4,
          url: "https://www.programmableweb.com/sites/default/files/random.dog_API_Image.jpg",
          isFavorite: false,
        },
    ]
  }
}
</script>
