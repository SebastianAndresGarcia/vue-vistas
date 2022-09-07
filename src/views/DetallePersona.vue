<template>
  <v-container class="grey lighten-2" flex fill-height>
    <v-row class="mb-6">
      <NavBarTop></NavBarTop>
    </v-row>
    <v-row class="mb-10" justify="center" align="center">
      <v-col md="4">
        <v-card>
          <v-list-item three-line>
            <v-list-item-content>
              <v-list-item-title class="text-h6 mb-1">
                Datos Personales
              </v-list-item-title>
            </v-list-item-content>
            <v-list-item-avatar tile size="150" color="grey">
              <v-img src="../assets/perfil.png" ></v-img>
            </v-list-item-avatar>
          </v-list-item>
          <v-list>
            <v-list-item>
              <v-list-item-action>
                <h4>Apellidos</h4>
              </v-list-item-action>

              <v-list-item-content>
                <v-list-item-title>García Martínez</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-action>
                <h4>Nombres</h4>
              </v-list-item-action>

              <v-list-item-content>
                <v-list-item-title>Sebastián Andrés</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-action>
                <h4>D.N.I. N°</h4>
              </v-list-item-action>

              <v-list-item-content>
                <v-list-item-title>33444555</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-action>
                <h4>Domicilio</h4>
              </v-list-item-action>

              <v-list-item-content>
                <v-list-item-title>Orlando, FL 79938</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-action>
                <v-icon>mdi-map-marker</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <mi-domicilio></mi-domicilio>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>

      <v-col class="white ml-10" md="6">
        <v-row class="mb-2 mt-2" justify="center">
          <v-col justify="center">
            <h3>Causas</h3>
          </v-col>
        </v-row>
        <v-divider></v-divider>
        <TablaCausas></TablaCausas>
      </v-col>
    </v-row>
    <v-divider inset></v-divider>
    <v-row class="grey lighten-2" md="12" justify="center">
      <PiePag></PiePag>
    </v-row>
    <EditorTexto></EditorTexto>
  </v-container>
</template>

<script>
import Vue from "vue";
import NavBarTop from "@/components/NavBarTop.vue";
import midomicilio from "@/components/midomicilio.vue";
import TablaCausas from "@/components/tablacausas.vue";
import PiePag from "@/components/piepagina.vue";

export default Vue.extend({
  name: "detalle-persona",

  data() {
    return {
      value: 1,
    };
  },
  components: {
    NavBarTop,
    "mi-domicilio": midomicilio,
    TablaCausas,
    PiePag,
  },
});
</script>
