<template>
  <v-row class="mb-2 mt-2" justify="center" align="center">
    <v-data-table
      :headers="headers"
      :items="causas"
      :items-per-page="5"
      search.sync="search"
      item-key="nrocausa"
      class="elevation-1 brown lighten-5"
      :footer-props="{
        showFirstLastPage: true,
        firstIcon: 'mdi-arrow-collapse-left',
        lastIcon: 'mdi-arrow-collapse-right',
        prevIcon: 'mdi-minus',
        nextIcon: 'mdi-plus',
      }"
    >
      <template #[`item.nrocausa`]="{ value }">
        <a :href="'/Caratula'">
          {{ value }}
        </a>
      </template>
    </v-data-table>
  </v-row>
</template>

<script>
export default {
  name: "TablaCausas",
  data() {
    return {
      headers: [
        {
          text: "Expte. N°",
          align: "start",
          value: "nrocausa",
        },
        { text: "Caratula", value: "caratula" },
        { text: "Fecha", value: "fecha" },
        { text: "Delito", value: "delito" },
        { text: "Carácter", value: "caracter" },
      ],
      causas: [
        {
          nrocausa: "1",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "2",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "denunciante",
        },
        {
          nrocausa: "3",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "imputado",
        },
        {
          nrocausa: "4",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "imputado",
        },
        {
          nrocausa: "5",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "6",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "denunciante",
        },
        {
          nrocausa: "7",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "8",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "9",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "10",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "11",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
        {
          nrocausa: "12",
          caratula: "F.C. NN P/Av. Delito",
          fecha: "01-01-2022",
          delito: "robo",
          caracter: "testigo",
        },
      ],
    };
  },
};
</script>
