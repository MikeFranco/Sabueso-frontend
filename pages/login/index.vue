<template>
    <section class="container"> 
        <div class="opacidad">
        </div>
    </section>
    
</template> 

<script>
export default {
    data(){
        return {
            bckImg: require('../../assets/login.jpg')
        }
    }
}
</script>

<style scoped>

.container {
  min-width: 100%;
  height: 100vh;
  background-image: url("../../assets/login.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  margin: 0;
  padding: 0;
}

.opacidad {
  background: rgba(0, 0, 0, 0.7);
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

</style>



