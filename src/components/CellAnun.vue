
<template>
    <v-col id="Cel-anuncios" xs="12" md="6" lg="4">
        <CardCell v-for="anuncio in cv19014Productos" :key="anuncio.id" :cv19014Productos="anuncio"/>
    </v-col>
</template>

<style lang="postcss" scoped>
    #Cel-anuncios {
        display: contents;
    }
</style>

<script>
    import CardCell from "./CardCell.vue";
    import { db } from "../db";
    export default {
        name: "CellAnun",
        components: {
            CardCell,
        },
        data() {
            return {
                cv19014Productos:[],
                cv19014ProductosOriginal: [],
            }
        },
        firestore: {
            cv19014Productos: db.collection('cv19014Productos'),
        },
        methods: {
            // Metodo para ordenar los productos en orden Ascendente
            OrdenarPrecio(Ascendente){
                this.cv19014Productos.sort((a,b)=>{
                    var retorno = 1;
                    if(a.Precio>b.Precio)
                        retorno = 1;
                    else if(a.Precio<b.Precio)
                        retorno = -1;
                    if(!Ascendente)
                        retorno = retorno *-1
                    return retorno;
                })
            },
            // Metodo para filtrar por un intervalo de precios
            FiltroIntervalo(IntervaloInicial, IntervaloFinal){
                if(this.cv19014ProductosOriginal.length == 0) {
                    this.cv19014ProductosOriginal = this.cv19014Productos.slice();
                }else {
                    this.cv19014Productos = this.cv19014ProductosOriginal.slice();
                }
                this.limpiar();
                this.cv19014Productos = this.cv19014Productos.filter((item) => {
                    if(item.Precio >= IntervaloInicial && item.Precio <= IntervaloFinal) {
                        return true;
                    }else {
                        return false;
                    }
                });
            },
            // Metodo para filtrar los celulares con un precio mayor a $500 USD
            Filtro500(){
                if(this.cv19014ProductosOriginal.length == 0) {
                    this.cv19014ProductosOriginal = this.cv19014Productos.slice();
                }else {
                    this.cv19014Productos = this.cv19014ProductosOriginal.slice();
                }
                this.limpiar();
                this.cv19014Productos = this.cv19014Productos.filter((item) => {
                    if(item.Precio >= 500) {
                        return true;
                    }else {
                        return false;
                    }
                });
            },
            // Metodo para reiniciar toda la busqueda
            FiltroReiniciar(){
                if(this.cv19014ProductosOriginal.length == 0) {
                    this.cv19014ProductosOriginal = this.cv19014Productos.slice();
                }else {
                    this.cv19014Productos = this.cv19014ProductosOriginal.slice();
                }
                this.limpiar();
                this.cv19014Productos = this.cv19014Productos.filter((item) => {
                    if(item.Precio >= 0) {
                        return true;
                    }else {
                        return false;
                    }
                });
            },
            //
            limpiar() {
                if (this.cv19014ProductosOriginal.length>0) {
                    this.cv19014Productos = this.cv19014ProductosOriginal.slice();
                }
            },
        },
        mounted() {
            this.cv19014ProductosOriginal=this.cv19014Productos.slice();
        },
    }
</script>