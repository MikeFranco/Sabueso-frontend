<template>
  <section>
    <div class="nav-bar" >
      <NavBar/> <!-- //TODO Hay que hacer este nav bar -->
    </div>
    <div>
      <!-- //TODO arreglar recorte de la imagen -->
      <img class="first-screen-img" src="../../assets/FSI_1.png"> 
    </div>
      <v-icon size="70" class="main-btn-left" >{{ pawIcon }}</v-icon>
      <v-icon size="70" class="main-btn-center" >{{ alertIcon }}</v-icon>
      <v-icon size="70" class="main-btn-right" >{{ homeIcon }}</v-icon>

    <div class="missing-dogs-div" >
      <MissingDogs/>
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
      homeIcon: 'mdi-home'
    }
  }
}
</script>

<style scoped>
.nav-bar {
  background-color:  #678BEC;
  color: azure;
}

.main-btn-left {
  margin-left: 18%
}

.main-btn-center,
.main-btn-right {
  margin-left: 25%
}

.first-screen-img {
  max-width: 100%;
  max-height: 25%;
}

.div-main-btns {
  text-align: center;
  
}

</style>