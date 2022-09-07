<template>
  <v-container class="grey lighten-2" fluid fill-height>
    <v-row class="mb-6">
      <NavBarTop></NavBarTop>
    </v-row>
    <v-row class="mb-10 md-12" md="12" justify="center" align="center">
      <v-col md="12" >
        <EditorTiny> </EditorTiny>
      </v-col>

    </v-row>
    <v-divider inset></v-divider>
    <v-row class="grey lighten-2" md="12" justify="center">
      <PiePag></PiePag>
    </v-row>
   
  </v-container>
</template>

<script>
import Vue from "vue";
import NavBarTop from "@/components/NavBarTop.vue";
import midomicilio from "@/components/midomicilio.vue";
import EditorTiny from "@/components/EditorTiny.vue";
import PiePag from "@/components/piepagina.vue";

export default Vue.extend({
  name: "EditorTexto",

  data() {
    return {
      value: 1,
    };
  },
  components: {
    NavBarTop,
    
    EditorTiny,
    PiePag,
  },
});
</script>
