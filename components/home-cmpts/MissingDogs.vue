<template>
  <section>
    <div class="dog-card">
      <div>
        <img :src="dog.img" :alt="dog.name" class="dog-image" >
        <div class="dog-name" > {{dog.name}} </div>
      </div>
        <div class="here-map" >
          <Map
            appId="DPVmzC3KXrz9Bk3wzpfR"
            appCode="xpxcR1OHlqPK043UfzNHZQ"
            lat="19.311274"
            lng="-99.176742"
            width="100%"
            height="200px"
          />
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
  text-align: center;
}

.dog-image {
  margin: auto auto;
  max-height: 300px;
  align-content: center;
}

.dog-name {
  background-color: #B21779;
  text-align: center;
  color: azure;
  font-weight: bold;
}

</style>