<template>
  <section>
    <div>
    <h1>Perros Extraviados</h1>
    <!-- <img :src="dogImg" alt="Esto murió"> -->
    <div v-for="(dog, index) in hardcodedItems" :key="index">
      {{dog.name}}
      {{dog.age}}
      {{dog.size}}
      <!-- <img :src="dog.img"> -->
      {{dog.description}}
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
</style>