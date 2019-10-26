<template>
  <section>
    <div class="nav-bar" >
      <NavBar/> <!-- //TODO Hay que hacer este nav bar -->
    </div>
    <div>
      <fa class="main-btn" :icon="[ 'fal', 'external-link-alt' ]" />
      <fa class="main-btn" :icon="[ 'fal', 'external-link-alt' ]" />
      <fa class="main-btn" :icon="[ 'fal', 'external-link-alt' ]" />
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';

export default {
  components: { NavBar }
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

</style>