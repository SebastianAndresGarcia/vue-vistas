<template>
  <v-toolbar dark style="max-height: 80px">
    <v-toolbar-title >
      <a :href="'/login'">
        <v-img src='images/logoNavBar.JPG' margin="1px" max-width="50%" max-height="50%"></v-img>
      </a>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    
    <v-form >
      <v-container fluid style="max-height: 80px">
      <v-row justify="center">
        <v-col 
          md="8">
          <v-text-field   ></v-text-field>
        </v-col>
        <v-col >
          <v-btn text>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
    </v-form>
    <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text href="/principal">
        Principal
      </v-btn>

      <v-divider vertical></v-divider>
      <v-btn text href="/MiPerfil">
        Mi Perfil
      </v-btn>
      <v-divider vertical></v-divider>
    </v-toolbar-items>

    <v-menu bottom left>
      <template v-slot:activator="{ on, attrs }">
        <v-btn dark icon v-bind="attrs" v-on="on">
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </template>

      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i">
          <a :href="'./' + item.value">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </a>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-toolbar>

</template>

<script >

import Vue from 'vue';
export default Vue.extend({
  name: 'NavBarTop',

  data() {
    return {
      loader: null,
      items: [
        { title: 'Ayuda', value: 'ayuda' },
        { title: 'Configuración', value: 'configuracion' },
        { title: 'Mi Perfil', value: 'perfil' },
        { title: 'Cerrar Sesión', value: 'login' },
      ],
    }
  },


})

</script>

<style lang=""></style>
