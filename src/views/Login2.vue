<template>
  <v-container class="image" flex fill-height>
    <v-row class="contenedor justify-center" align="center">
      <v-col md="7" align="center"> </v-col>
      <v-col md="5" class="menu justify-center" align="center">
        <div class="shadow">
          <v-row class="justify-center" align="center">
            <v-col class="" align="center" justify="center">
              <v-img max-width="50%" max-height="60%" src="images/logoMP.JPG"></v-img>
            </v-col>
          </v-row>
          <v-row class="justify-center">
            <v-col class="" md="6">
              <v-form ref="form" v-model="valid" lazy-validation>
                <v-row class="mb-6 mt-6">
                  <v-text-field
                    v-model="usuario"
                    :rules="nameRules"
                    label="Usuario"
                    required
                  ></v-text-field>

                  <v-text-field
                    v-model="password"
                    :rules="passRules"
                    label="Clave"
                    required
                  ></v-text-field>
                </v-row>
                <v-row class="mt-12 justify-center" align="center">
                  <v-col class="" md="12">
                    <v-btn :disabled="!valid" color="success" class="" @click="validate">
                      Ingresar
                    </v-btn></v-col
                  >
                  <v-col class="" md="12"><v-btn text small>Olvidé mi clave </v-btn></v-col>
                </v-row>
              </v-form>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
    <!--<v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset Form
    </v-btn>

    <v-btn
      color="warning"
      @click="resetValidation"
    >
      Reset Validation
    </v-btn>  -->
  </v-container>
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  name: "log-in2",

  data() {
    return {
      valid: true,
      nameRules: [(v) => !!v || "Usuario es requerido"],
      passRules: [(v) => !!v || "Ingrese contraseña"],
    };
  },
  methods: {
    validate() {
      this.$refs.form.validate();
    },
    reset() {
      this.$refs.form.reset();
    },
    resetValidation() {
      this.$refs.form.resetValidation();
    },
  },
});
</script>

<style>
.shadow {
  padding: 40px;
}
.image {
  background-image: url("../assets/mpf.jpeg");
  background-size: 60% 100%, cover;
  background-repeat: no-repeat;
  position: absolute;
}
/*.contenedor {
    background-color: #fff;
    overflow: hidden;
    width: 780px;
    margin: 10px auto 5px auto;
    
}
.content {
    background-color: #fff;
    width: 580px;
    border-right: 200px solid #0099FF; 
    margin-right: -200px;
    float: left;
}
.menu {
    width: 200px;
    float: left;
    color: #fff;
    background: #0099FF;
    text-align: left;
    
} */
</style>
