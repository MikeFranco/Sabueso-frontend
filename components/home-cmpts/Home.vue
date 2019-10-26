<template>
  <section>
    <div class="nav-bar" >
      <NavBar/> <!-- //TODO Hay que hacer este nav bar -->
    </div>
    <div>
      <fa :icon="[ 'fal', 'external-link-alt' ]" />
      <fa :icon="[ 'fal', 'external-link-alt' ]" />
      <fa :icon="[ 'fal', 'external-link-alt' ]" />
    </div>
  </section>
</template>

<script>
import NavBar from '~/components/generic-cmpts/NavBar.vue';

export default {
  components: { NavBar }
}
</script>

<style>
.nav-bar {
  background-color: red;
}
</style>