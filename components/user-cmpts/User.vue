<template>
  <section>
    <NavBar />
    <section class="user-container" >
      <div class="user-info">
        <img class="user-img" :src="user.img" :alt="user.name">
        <div class="user-full-name" >
          <span class="user-name" > {{ user.name }} </span><br/>
          <span class="user-last-name"> {{ user.lastName }} </span>
        </div>
      </div>
      <div class="global-dog-container" >
        <div class="row dog-card-container">
            <DogInfo
              class="col-md-8 align-items-stretch "
              v-for="(dog, index) in user.pets"
              :key="index"
              :dog="dog"
            />
        </div>
      </div>
    </section>
  </section>
</template>

<script>
import NavBar from '../generic-cmpts/NavBar.vue';
import DogInfo from '../generic-cmpts/DogInfo.vue';

export default {
  components: { NavBar, DogInfo },
  //props:['user'],
  data() {
    return {
      user:{
        name: 'Mariana',
        lastName: 'Ruiz de Chávez Tamayo',
        img: require('../../assets/yorkshire-mini.jpg'),
        pets:[{name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
        {name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')},{name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')},{name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')},
          {name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
          {name: 'Koda', age: 5, size: 'inmensurable',
          description: 'Una descripción hardcodeada', img:require('../../assets/Koda.jpg')},
          {name: 'Chip', age: 5, size: 'microchip',
          description: 'Una descripción hardcodeada2', img:require('../../assets/Chip.jpg')}
        ]
      }
    }
  }


}
</script>

<style scoped>
.user-img {
  border-radius: 50%;
}

.user-name{
  font-size: 50px;
}

.user-last-name {
  font-size: 25px;
}

.user-pets {
  background-color: #678BEC;
}

.user-container {
  display: flex;
}

.user-full-name {
  text-align: center;
}

.user-info {
  width: 50%;
  padding-left: 10%;
}

.global-dog-container {
  padding-right: 2%;
}

/* CSS del componente de home */
.nav-bar {
  background-color:  #678BEC;
  color: white;
  max-width: 100%;
}

.active{
  color: #678BEC;
}

.dog-card-container{
  max-height: 500px;
  width: 80%;
  overflow-y: auto;
}
.main-btn-left {
  margin-left: 18%
}

.main-btn-center,
.main-btn-right {
  margin-left: 25%
}

.missing-dogs-title {
  text-align: center;
  font-size: 38px;
  color: white;
  background-color: #678BEC;
  margin-top: 2%;
  padding-top: 1%;
  padding-bottom: 0.7%;
}

/* .main-btn-center:hover,
.main-btn-right:hover,
.main-btn-left:hover{
  background-color: #678BEC;
} */

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