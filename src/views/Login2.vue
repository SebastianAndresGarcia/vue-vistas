<template>
  <v-container flex fill-height class="teal lighten-4">
    <v-row class="justify-center" align="center">
      <v-col class="white justify-center" align="center" md="3">
        <v-row class="justify-center" align="center">
          <v-col class="" align="center" justify="center">
            <v-img max-width="80%" max-height="80%" src="images/logoMP.JPG"></v-img>
          </v-col>
        </v-row>
        <v-row class="justify-center">
          <v-col class="" md="8">
            <v-form ref="form" v-model="valid" lazy-validation>
              <v-text-field v-model="usuario" :rules="nameRules" label="Usuario" required></v-text-field>

              <v-text-field v-model="password" :rules="passRules" label="Clave" required></v-text-field>

              <v-btn :disabled="!valid" color="success" class="" @click="validate">
                Ingresar
              </v-btn>

            </v-form>
          </v-col>
        </v-row>
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
