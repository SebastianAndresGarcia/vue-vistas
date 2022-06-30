<template>

  <v-toolbar color="blue" dark>
    <v-toolbar-title>

      Ministerio Público Fiscal de Mendoza

    </v-toolbar-title>

    <v-divider class="mx-6" vertical></v-divider>

<v-text-field
        hide-details
        prepend-icon="mdi-magnify"
        single-line
      ></v-text-field>

      <v-btn text>
        Busqueda
      </v-btn>

    <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text href="/principal">
        Principal
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn text href="/Configuracion">
        Configuracion
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn text href="/Ayuda">
        Ayuda
      </v-btn>

      <v-divider vertical></v-divider>
      <v-btn text href="/Ayuda">
        Mi Perfil
      </v-btn>
      <v-divider vertical></v-divider>
    </v-toolbar-items>

    <v-app-bar-nav-icon></v-app-bar-nav-icon>
  </v-toolbar>
</template>

<script >


export default {
  data: () => ({ value: 1 }),
}

</script>

<style lang=""></style>
