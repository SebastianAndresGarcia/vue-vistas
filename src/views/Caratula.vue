<template>
  <v-container class="white" flex >
    <v-row class="mb-6">
      <!-- mb es margin bottom-->
      <NavBarTop></NavBarTop>
    </v-row>

    <v-row class="mb-2 justify-center">
      <v-col md="2" xs3 >
        <h3><b>Expediente:</b></h3>
      </v-col>
      <v-col style="height:40px" md="7" xs3 >
        <h3>P-111/22</h3>
      </v-col>
      <v-col style="height:60px" md="3" xs3 align="center">
        <v-btn depressed color="success">
          Instruir
        </v-btn>
      </v-col>
    </v-row>
    <v-divider></v-divider>
    <v-row class="mb-2  mt-2 justify-center">
      <v-col style="height:50px" md="2" xs3>
        <h3>Caratula: </h3>
      </v-col>
      <v-col md="10" xs3>
        <p><b>"FISCAL C/NN y ots P/AV. HECHO"</b></p>
      </v-col>
    </v-row>
    <v-divider></v-divider>
    <v-row class="mb-2 mt-2 justify-center">
      <v-col md="2" xs3 >
        <h3><b>Fiscalía:</b></h3>
      </v-col>
      <v-col  md="6" xs3 >
        <p>Unidad Fiscal Robos, Hurtos Agravados y Sustracción de Automotores</p>
        <p>Fiscalía de Instrucción N° 29</p>
      </v-col>
      <v-col md="1" xs3 align="center">
        <h3><b>Fiscal:</b></h3>
      </v-col>
      <v-col md="3" xs3 align="left">
        <h3><b>Dr. Pepe Pep</b></h3>
      </v-col>
    </v-row>

    <v-divider></v-divider>
    <v-row style="height:150px" class=" mb-2 mt-2 justify-center">
      <v-col style="height:50px" md="2" xs3>
        <h3>Imputados: </h3>
      </v-col>
      <v-col md="10" xs3>
        <p>Juan Perez</p>
        <p>José Lopez</p>
        <p>Pepe Gomez</p>
      </v-col>
    </v-row>
    <v-divider></v-divider>
    <v-row class="justify-center teal lighten-4">
      <v-col md="2" xs3 >
        <h3>Vencimientos:</h3>
      </v-col>
      <v-col md="4" xs3 >
        <p>../../..</p>
        <p>../../..</p>
        <p>../../..</p>
      </v-col>
      <v-col md="1" xs3>
        <h3>Delitos</h3>
      </v-col>
      <v-col md="5" xs3 >
        <p>Delito 1</p>
        <p>Delito 2</p>
        <p>Delito 3</p>
      </v-col>
    </v-row>
    <v-divider class="mt-2"></v-divider>
    <v-row class="mb-2 mt-2 justify-center">
      <v-col md="2" class="">
        <h3>Actividades</h3>
      </v-col>
      <v-col md="4" xs3 class=" ">
        <v-card max-width="344">
            <v-container flex>
              <v-checkbox v-model="uer" label="Solicitud UER" color="green" value="uer" hide-details></v-checkbox>
              <v-checkbox v-model="rnr" label="Solicitud RNR" color="green" value="rnr" hide-details></v-checkbox>
              <v-checkbox v-model="rphgd" label="Muestra RPHGD" color="green" value="rphgd" hide-details></v-checkbox>
              <v-checkbox v-model="cmf" label="Solicitud Informe CMF" color="green" value="cmf" hide-details></v-checkbox>
              <v-checkbox v-model="udapif" label="Solicitud Informe UDAPIF" color="green" value="udapif" hide-details></v-checkbox>
            </v-container>
        </v-card>

      </v-col>
      <v-col md="2" xs3 class=" ">
        <h3>Destacados:</h3>
      </v-col>
      <v-col md="4" xs3 class=" ">
        <p align="justify">Acá van las observaciones, detalles, recordatorios, etc, etc.
          Acá van las observaciones, detalles, recordatorios, etc, etc.
          Acá van las observaciones, detalles, recordatorios, etc, etc.
          Acá van las observaciones, detalles, recordatorios, etc, etc.
          Acá van las observaciones, detalles, recordatorios, etc, etc.
        </p>
      </v-col>
    </v-row>
    <v-divider ></v-divider>
    <v-row class="mt-2 mb-4 grey lighten-2" justify="center">
      <PiePag></PiePag>
    </v-row>
  </v-container>
</template>

<script >
import Vue from 'vue';
import NavBarTop from '@/components/NavBarTop.vue'
import PiePag from "@/components/piepagina.vue";
export default Vue.extend({
  name: 'caratula-1',

  data: () => ({
    //
  }),
  components: {
    NavBarTop,
    PiePag
  }
});

</script>