<template>
  <v-toolbar dark >
    <v-toolbar-title>
      <a :href="'/login2'">
        <v-img
          src="images/logoNavBar.JPG"
          margin="1px"
          max-width="50%"
          max-height="50%"
        ></v-img>
      </a>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar floating>
      <v-form>
        <v-row>
          <v-col md="8">
            <v-text-field  hide-details single-line></v-text-field>
          </v-col>
          <v-col>
            <v-btn>
              <v-icon>mdi-magnify</v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-form>
    </v-toolbar>
    <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text href="/principal"> Principal </v-btn>

      <v-divider vertical></v-divider>
      <v-btn text href="/MiPerfil"> Mi Perfil </v-btn>
      <v-divider vertical></v-divider>
    </v-toolbar-items>

    <!-- <v-menu bottom left>
      <template v-slot:activator="{ on, attrs }">
        <v-btn dark icon v-bind="attrs" v-on="on">
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-btn class="ma-1 dark" 
                icon
        plain :href="'./' + item.value">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-btn>
        </v-list-item>
      </v-list>
    </v-menu> -->
    <v-menu bottom left>
      <template v-slot:activator="{ on, attrs }">
        <v-btn dark icon v-bind="attrs" v-on="on">
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </v-btn>
      </template>

      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :href="'./' + item.value">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-toolbar>
</template>

<script>
import Vue from "vue";
export default Vue.extend({
  name: "NavBarTop",

  data() {
    return {
      loader: null,
      items: [
        { title: "Ayuda", value: "ayuda" },
        { title: "Configuración", value: "configuracion" },
        { title: "Mi Perfil", value: "perfil" },
        { title: "Cerrar Sesión", value: "login2" },
      ],
    };
  },
});
</script>

<style lang=""></style>
