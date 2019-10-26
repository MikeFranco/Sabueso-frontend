<template>
  <section>
    <div class="dog-car">
      <div class="container">
        <div class="row">
          <div>
            <img :src="dog.img" :alt="dog.name" class="dog-image" >
            <div class="dog-name" > {{dog.name}} </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props:['dog']

}
</script>

<style>
.dog-card {
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.18);
  border-radius: 3px;
  margin-top: 20px;
  margin-bottom: 20px;
  padding-top: 15px;
}

.dog-image {
  margin: auto auto;
  max-height: 300px;
}

.dog-name {
  background-color: #B21779;
  text-align: center;
  color: azure;
  font-weight: bold;
}
</style>