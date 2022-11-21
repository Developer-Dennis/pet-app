<template>
  <div class="home"></div>
  <Pets  :pets="pets" />
</template>

<script>
import Pets from '../components/Pets.vue'
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    Pets
  },
  data(){
    return{
      pets:[
        {
          id:1,
          name: "Ruby",
          age:2,
          img: "https://ywz5lk6v0z.csb.app/",
          isFavorite: true,
        },
        {
          id:2,
          name: "CoCo",
          age:4,
          img: "https://ywz5lk6v0z.csb.app/",
          isFavorite: false,
        },
      ],
    }
  }
}
</script>
