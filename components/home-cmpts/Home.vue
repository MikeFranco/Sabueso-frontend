<template>
  <section>
    <div class="nav-bar">
      <NavBar/>
    </div>
    <div>
      <img class="first-screen-img" src="../../assets/FSI_1.png">
    </div>
      <img class="main-btn-left" src="../../assets/Alerta.png" alt="activar alerta">
      <img class="main-btn-center" src="../../assets/Paw.png" alt="adopción">
      <img class="main-btn-right" src="../../assets/Casa.png" alt="dar en adopción">

    <div class="missing-dogs-div" >
      <div class="missing-dogs-title" >
        <h1>PERROS EXTRAVIADOS</h1>
      </div>
      <div class="dog-card-container">
        <div class="inner-card-container">
          <MissingDogs
            class="dog-card-swiper col-md-6"
            v-for="(dog, index) in hardcodedItems"
            :key="index"
            :dog="dog"
          />
        </div>
      </div>
    </div>

    <h1 class="adopt-title" >¡ADOPTA A UN COMPAÑERO!</h1>
    <div class="adopt">
      <DogInfoHome
        class="col-md-4 d-flex align-items-stretch "
        v-for="(dog, index) in hardcodedItems"
        :key="index"
        :dog="dog"
        :showMap="false"
      />
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';
import MissingDogs from '~/components/home-cmpts/MissingDogs.vue';
import DogInfoHome from '~/components/generic-cmpts/DogInfoHome.vue';

export default {
  components: { NavBar, MissingDogs, DogInfoHome },
  props:['missingPets'],
  data(){
    return {
      pawIcon: 'mdi-paw',
      alertIcon: 'mdi-alert',
      homeIcon: 'mdi-home',
      hover: false,
      hardcodedItems:[
          {name: 'Koda', age: 5, size: 'Grande',
          description: 'Pastor Belga', img:require('../../assets/Koda.jpg')},
          {name: 'Manchas', age: 1, size: 'Pequeño',
          description: 'Boston terrier', img:require('../../assets/perrito1.jpg')},
          {name: 'Link', age: 3, size: 'Pequeño',
          description: 'Maltipo blanco', img:require('../../assets/perrito2.jpg')},
          {name: 'Negro', age: 7, size: 'Grande',
          description: 'Whippet café', img:require('../../assets/perrito3.jpg')}
      ],
    }
  }
}
</script>

<style scoped>
.nav-bar {
  background-color:  #678BEC;
  color: white;
  max-width: 100%;
}

.active{
  color: #678BEC;
}

.dog-card-container{
  background-color: #678BEC;
  padding: 30px;
  max-height: 450px;
  width: 100%;
  overflow-x: auto;
  overflow-y: hidden;
}

.adopt {
  display: flex;
  background-color: white;
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
  padding-right: 2%;
  margin: center;
  margin-left: 50px;
}

.main-btn-center,
.main-btn-right {
  margin-left: 10%
}

.dog-card-swiper {
  max-width: 120%;
  min-width: 80%;
  max-height: 100%;
  padding-right: 5%;

}

.missing-dogs-title {
  text-align: center;
  font-size: 38px;
  color: white;
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
  background-color: white;
}

.adopt-title {
  color: #B21779;
  background-color: white;
  text-align: center;
  padding-top: 2%;
  padding-bottom: 1%;
  text-align: center;
  font-size: 57px;
  margin-top: 2%;
  padding-top: 1%;
  padding-bottom: 0.7%;
}

</style>