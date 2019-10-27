<template>
  <section>
    <div class="dog-card">
      <div :style='`background-image: url(${dog.img})`' class="dog-image" >
      </div>
      <div class="dog-text" >
        {{dog.description}}
      </div>
    </div>
  </section>
</template>

<script>
import Map from '../generic-cmpts/Map.vue';
export default {
  components: { Map },
  props:['dog']

}
</script>

<style scoped>

.dog-card {
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.18);
  border-radius: 30px;
  overflow: hidden;
  text-align: center;
  display: flex;
}

.dog-image {
  margin: auto auto;
  height: 200px;
  background-position: center;
  background-size: cover;
  min-width: 33%;
  align-items: left;
}

.dog-text {
  flex:1;
}

.dog-name {
  background-color: #B21779;
  text-align: center;
  color: azure;
  font-weight: bold;
  font-size: 25px;
}

.here-map {
  min-width: 100%;
}

</style>