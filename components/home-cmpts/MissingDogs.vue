<template>
  <section>
    <div>
      <h1>Perros Extraviados</h1>
      <div class="row" >
        <div class="col-md-9" > <!-- //TODO Terminar este css para que sean un renglón los n perros  -->
          <div class="dog-card" v-for="(dog, index) in hardcodedItems" :key="index">
            <img class="dog-img" :src="dog.img">
            <div class="dog-name" > {{dog.name}} </div>
            <div class="dog-extra-data">
            {{dog.age}}
            {{dog.size}}
            {{dog.description}}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data(){
    return {
      hardcodedItems:[
        {name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
        {name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')}
      ],
      dogImg: '../../assets/yorkshire-mini.jpg'
    }
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  margin-top: 2%;
  font-size: 50px;
  color: azure;
}

div {
  background-color: #678BEC;
}

.dog-img {
  max-width: 200px;
  max-height: 210px;
  vertical-align: center;
}

.dog-name {
  background-color: #B21779;
  text-align: center;
  color: azure;
  font-weight: bold;
}

.dog-card {
  max-width: 15%;
  background-color: red;
}

.dog-extra-data {
  background-color: azure;
}
</style>