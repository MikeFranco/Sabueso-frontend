<template>
  <section>
    <div class="nav-bar" >
      <NavBar/> <!-- //TODO Hay que hacer este nav bar -->
    </div>
    <div>
      <!-- //TODO arreglar recorte de la imagen -->
      <img class="first-screen-img" src="../../assets/FSI_1.png"> 
    </div>
      <button class="main-btn-center"> <v-icon size="70">{{ alertIcon }} </v-icon> </button>
      <button class="main-btn-left">   <v-icon size="70">{{ pawIcon }} </v-icon> </button>
      <button class="main-btn-right">  <v-icon size="70">{{ homeIcon }} </v-icon> </button>

    <div class="missing-dogs-div" >
       <div class="row  dog-card-container" style="margin-top:30px; border-top:1px solid #d9d9d9;">
        <MissingDogs
          class="col-md-4 d-flex align-items-stretch "
          v-for="(dog, index) in hardcodedItems"
          :key="index"
          :dog="dog"
        />
      </div>
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';
import MissingDogs from '~/components/home-cmpts/MissingDogs.vue';

export default {
  components: { NavBar, MissingDogs },
  data(){
    return {
      pawIcon: 'mdi-paw',
      alertIcon: 'mdi-alert',
      homeIcon: 'mdi-home',
      hover: false,
      hardcodedItems:[
        {name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
        {name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')},{name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')},{name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')},
          {name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
          {name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
          {name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')}
      ],
    }
  }
}
</script>

<style scoped>
.nav-bar {
  background-color:  #678BEC;
  color: azure;
}

.active{
  color: #678BEC;
}

.dog-card-container{
  background-color: #678BEC;
}
.main-btn-left {
  margin-left: 18%
}

.main-btn-center,
.main-btn-right {
  margin-left: 25%
}

.main-btn-center:hover,
.main-btn-right:hover,
.main-btn-left:hover{
  background-color: #678BEC;
}

.first-screen-img {
  max-width: 100%;
  max-height: 25%;
}

.div-main-btns {
  text-align: center;
}

button{
  border-radius: 50px;
}

</style>