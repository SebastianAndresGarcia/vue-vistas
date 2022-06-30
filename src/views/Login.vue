<template>

    <section class="section-container">
        <v-row class="signin">
            <v-col cols="8" class="left">
                <v-img lazy-src='images/logoMP2.JPG' max-height="90%" max-width="90%" src='images/logoMP2.JPG'></v-img>
            </v-col>
            <v-col cols="4" class="right">
                <h3>INICIAR SESION</h3>

                <v-form @submit.prevent="submit">

                    <v-text-field v-model="email" :error-messages="errors" label="Usuario" required outlined dark filled
                        dense></v-text-field>


                    <v-text-field v-model="password" :error-messages="errors" label="Contraseña"
                        :append-icon="showPass ? 'mdi-eye' : 'mdi-eye-off'" @click:append="showPass = !showPass"
                        required outlined dense dark filled :type="showPass ? 'text' : 'password'">
                    </v-text-field>

                    <div class="text-center">
                        <v-btn class="signin-btn" type="submit" rounded color="white" dark>
                            Ingresar
                        </v-btn>
                    </div>
                </v-form>

            </v-col>
        </v-row>
    </section>


</template>

<script >

import Vue from 'vue';

export default Vue.extend({
    name: 'log-in',

    data() {
        return {
            loader: null,
        }
    },


})



</script>
