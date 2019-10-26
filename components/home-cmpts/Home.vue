<template>
  <section>
    <div class="nav-bar" >
      <NavBar/> <!-- //TODO Hay que hacer este nav bar -->
    </div>
    <div>
      <!-- //TODO arreglar recorte de la imagen -->
      <img class="first-screen-img" src="../../assets/FSI_1.png"> 
    </div>
    <div class="div-main-btns" >
      <fa class="main-btn main-btn-left" :icon="[ 'fal', 'external-link-alt' ]" />
      <fa class="main-btn main-btn-center" :icon="[ 'fal', 'external-link-alt' ]" />
      <fa class="main-btn main-btn-right" :icon="[ 'fal', 'external-link-alt' ]" />
    </div>

    <div class="missing-dogs-div" >
      <MissingDogs/>
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';
import MissingDogs from '~/components/home-cmpts/MissingDogs.vue';

export default {
  components: { NavBar, MissingDogs }
}
</script>

<style scoped>
.nav-bar {
  background-color:  #678BEC;
  color: azure;
}

.main-btn {
  font-size: 50px;
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