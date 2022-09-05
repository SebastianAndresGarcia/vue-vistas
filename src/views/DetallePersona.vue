<template>
    <v-container class="grey lighten-2" flex>
        <v-row class="mb-4">
            <NavBarTop></NavBarTop>
        </v-row>
        <v-row class="mb-4" justify="center" align="center">
            <v-col md="4">
                <v-card>
                    <v-list-item three-line>
                        <v-list-item-content>
                            <v-list-item-title class="text-h6 mb-1">
                                Datos Personales
                            </v-list-item-title>
                        </v-list-item-content>
                        <v-list-item-avatar tile size="150" color="grey">
                            <v-img src="https://picsum.photos/700?image=996" alt='images/logoMP2.JPG'></v-img>
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
                                <h4> D.N.I. N°</h4>
                            </v-list-item-action>

                            <v-list-item-content>
                                <v-list-item-title>33444555</v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>

                        <v-divider inset></v-divider>

                        <v-list-item>
                            <v-list-item-action>
                                <h4>Domicilio </h4>
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
               
                <v-row class="mb-2 mt-2" justify="center" align="center">
                    <v-data-table :headers="headers" :items="causas" :items-per-page="5" search.sync="search"
                        item-key="nrocausa" class="elevation-1 blue-grey lighten-4" :footer-props="{
                            showFirstLastPage: true,
                            firstIcon: 'mdi-arrow-collapse-left',
                            lastIcon: 'mdi-arrow-collapse-right',
                            prevIcon: 'mdi-minus',
                            nextIcon: 'mdi-plus'
                        }">
                        <template #[`item.nrocausa`]="{ value }">
                            <a :href="'/Caratula'">
                                {{ value }}
                            </a>
                        </template>

                    </v-data-table>
                </v-row>
            </v-col>
          
        </v-row>
        <v-divider></v-divider>
        <v-row class="mt-1" justify="center" align="center">
            <a>www.jus.mendoza.gov.ar</a>
        </v-row>
    </v-container>
</template>

<script >
import Vue from 'vue';
import NavBarTop from '@/components/NavBarTop.vue'
import midomicilio from "@/components/midomicilio.vue";
export default Vue.extend({
    name: 'detalle-persona',

    data() {
        return {
            headers: [
                {
                    text: 'Expte. N°',
                    align: 'start',
                    value: 'nrocausa',
                },
                { text: 'Caratula', value: 'caratula' },
                { text: 'Fecha', value: 'fecha' },
                { text: 'Delito', value: 'delito' },
                { text: 'Carácter', value: 'caracter'},
            ],
            causas: [
                {
                    nrocausa: '1',
                    caratula: 'Ice cream',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'testigo'
                },
                {
                    nrocausa: '2',
                    caratula: 'Ice cream',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'denunciante'
                },
                {
                    nrocausa: '3',
                    caratula: 'Cookie',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'imputado'
                },
                {
                    nrocausa: '4',
                    caratula: 'Pastry',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'imputado'
                },
                {
                    nrocausa: '5',
                    caratula: 'Cookie',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'testigo'
                },
                {
                    nrocausa: '6',
                    caratula: 'Candy',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'denunciante'
                },
                {
                    nrocausa: '7',
                    caratula: 'Candy',
                    fecha: '01-01-2022',
                    delito: 'robo',
                    caracter: 'testigo'
                }
            ],
        }
    },
    components: {
        NavBarTop,
        "mi-domicilio": midomicilio,
    }
});

</script>