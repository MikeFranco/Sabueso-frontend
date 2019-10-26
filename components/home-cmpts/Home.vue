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
      <MissingDogs/>
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';
import MissingDogs from '~/components/home-cmpts/MissingDogs.vue';
import Map from '~/components/generic-cmpts/Map.vue';

export default {
  components: { NavBar, MissingDogs, Map },
  data(){
    return {
      pawIcon: 'mdi-paw',
      alertIcon: 'mdi-alert',
      homeIcon: 'mdi-home',
      hover: false
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