<template>
    <section class="container"> 
        <div class="opacidad">
        <v-app id="inspire">
    <v-form
    class="form"
      ref="form"
      v-model="valid"
      lazy-validation
    >
      <v-text-field
        v-model="name"
        :counter="10"
        :rules="nameRules"
        label="Nombre"
        required
      ></v-text-field>

      <v-text-field
        v-model="lastname"
        :counter="10"
        :rules="lastnameRules"
        label="Apellido"
        required
      ></v-text-field>
  
      <v-text-field
        v-model="email"
        :rules="emailRules"
        label="E-mail"
        required
      ></v-text-field>
      
      <v-text-field
        v-model="celphone"
        :rules="celphonelRules"
        label="Celular"
        required
      ></v-text-field>
      
      <v-text-field
        v-model="email"
        :rules="emailRules"
        label="E-mail"
        required
      ></v-text-field>

  
      <v-select
        v-model="select"
        :items="items"
        :rules="[v => !!v || 'Item is required']"
        label="Talla"
        required
      ></v-select>
  
      <v-checkbox
        v-model="checkbox"
        :rules="[v => !!v || 'You must agree to continue!']"
        label="¿Aceptas terminos y condiciones de nuestro aviso de privacidad?"
        required
      ></v-checkbox>

      
  
      <v-btn
        color="#B21779"
        class="mr-4"
        @click="reset"
      >
        Reset Form
      </v-btn>
  
    </v-form>
  </v-app>
        </div>
        
    </section>
    
</template> 

<script>
export default {
    data(){
        return {
            bckImg: require('../../assets/login.jpg'), valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => (v && v.length <= 10) || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
    ],
    select: null,
    items: [
      'Pequeña', 
      'Mediana',
      'Grande',
    ],
    checkbox: false,
        }
    }, methods: {
    validate () {
      if (this.$refs.form.validate()) {
        this.snackbar = true
      }
    },
    reset () {
      this.$refs.form.reset()
    },
    resetValidation () {
      this.$refs.form.resetValidation()
    },
  },
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

.form {
    width: 500px;
    height: 500px;
    padding: 20px;
    margin: 10px;
}
#inspire {
    background: 0;}
    

</style>



