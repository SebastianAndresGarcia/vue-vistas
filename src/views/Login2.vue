<template>
  <section class="container-login2">
    <v-col class="signin">
      <v-row class="logo">
        <v-img max-height="10%" max-width="10%" src="images/logoMP.JPG"></v-img>
      </v-row>
      <v-row class="formlogin2">
        <v-form  ref="form" v-model="valid" lazy-validation>
          <v-text-field
            v-model="usuario"
            :rules="nameRules"
            label="Usuario"
            required
          ></v-text-field>

          <v-text-field
            v-model="password"
            :rules="passRules"
            label="clave"
            required
          ></v-text-field>

          <v-btn :disabled="!valid" color="success" class="mr-4" @click="validate">
            Ingresar
          </v-btn>

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
        </v-form>
      </v-row>
    </v-col>
  </section>
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  name: "log-in2",

  data() {
    return {
      valid: true,
      nameRules: [(v) => !!v || "Usuario es requerido"],
      passRules: [(v) => !!v || "Contraseña requerido"],
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
