<template>
  <section>
    <div class="nav-bar">
      <NavBar/> <!-- //TODO Hay que hacer este nav bar -->
    </div>
    <div>
      <!-- //TODO arreglar esta imagen porque  -->
      <img class="first-screen-img" src="../../assets/FSI_1.png">
    </div>
      <button class="main-btn-left"> <v-icon size="70">{{ alertIcon }} </v-icon> </button>
      <button class="main-btn-center">   <v-icon size="70">{{ pawIcon }} </v-icon> </button>
      <button class="main-btn-right">  <v-icon size="70">{{ homeIcon }} </v-icon> </button>

    <div class="missing-dogs-div" >
      <div class="missing-dogs-title" >
        <h1>Perros Extraviados</h1>
      </div>
      <div class="dog-card-container">
        <div class="inner-card-container">
          <MissingDogs
            class="dog-card-swiper"
            v-for="(dog, index) in hardcodedItems"
            :key="index"
            :dog="dog"
          />
        </div>
      </div>
    </div>

    <div class="adopt">
      <DogInfo
        class="col-md-4 d-flex align-items-stretch "
        v-for="(dog, index) in hardcodedItems"
        :key="index"
        :dog="dog"
      />
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';
import MissingDogs from '~/components/home-cmpts/MissingDogs.vue';
import DogInfo from '~/components/generic-cmpts/DogInfo.vue';

export default {
  components: { NavBar, MissingDogs, DogInfo },
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
  max-width: 100%;
}

.active{
  color: #678BEC;
}

.dog-card-container{
  background-color: #678BEC;
  padding: 30px;
  max-height: 500px;
  width: 100%;
  overflow: hidden;
}

.adopt {
  display: flex;
}

.adopt-card {
  flex: 1;
  width: 50%
}

.missing-dogs-div {
  height: 500px;
}

.main-btn-left {
  margin-left: 18%
}

.inner-card-container{
  display: flex;
  flex-wrap: nowrap;
  position: relative;
  min-height: 500px;
  max-width: 50%;
  padding-right: 2%
}

.main-btn-center,
.main-btn-right {
  margin-left: 25%
}

.dog-card-swiper {
  min-width: 100%;
  min-height: 350px;
  padding-right: 5%
}

.missing-dogs-title {
  text-align: center;
  font-size: 38px;
  color: azure;
  background-color: #678BEC;
  margin-top: 2%;
  padding-top: 1%;
  padding-bottom: 0.7%;
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

.adopt {
  background-color: azure;
}

</style>