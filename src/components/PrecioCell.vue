<template>
    <v-row id="Filtro-content" class="spacing-playground pa-0 rounded-xl">
        <v-col id="Filtro-tittle" cols="2"  class="d-none d-sm-flex">
            <h1 id="Texto-button" class="subtitle-2">
                FILTRAR PRECIOS
            </h1>
        </v-col>
        <div id="Divisor-content" class="d-none d-sm-flex">
            <v-divider id="Filtro-divisores" vertical></v-divider>
        </div>
        <v-col id="Filtro-inputs" cols="2" class="d-none d-sm-flex">
            <v-text-field
                color="red"
                label="Desde"
                type="number"
                v-model="IntervaloInicial"
                required
            ></v-text-field>
        </v-col>
        <v-col id="Filtro-inputs" cols="2" class="d-none d-sm-flex">
            <v-text-field
                color="red"
                label="Hasta"
                type="number"
                v-model="IntervaloFinal"
                required
            ></v-text-field>
        </v-col>
        <v-col id="Filtro-button" cols="4" lg="2">
            <v-btn @click="FiltroIntervalo" id="Button" class="rounded-pill" depressed>
                <i class='bx bx-check-circle bx-flashing bx-sm d-none d-sm-flex'></i>
                <h1 id="Texto-button" class="subtitle-2">Filtrar</h1>
            </v-btn>
        </v-col>
        <v-col id="Filtro-button" cols="4" lg="2">
            <v-btn @click="Filtro500" id="Button" class="rounded-pill" depressed>
                <i class='bx bx-dollar-circle bx-flashing bx-sm d-none d-sm-flex'></i>
                <h1 id="Texto-button" class="subtitle-2">+ de $500</h1>
            </v-btn>
        </v-col>
        <v-col id="Filtro-button" cols="4" lg="2">
            <v-btn @click="FiltroReiniciar" id="Button" class="rounded-pill" depressed>
                <i class='bx bx-reset bx-flashing bx-sm d-none d-sm-flex'></i>
                <h1 id="Texto-button" class="subtitle-2">Reiniciar</h1>
            </v-btn>
        </v-col>
    </v-row>
</template>

<style lang="less" scoped>
    #Filtro-content {
        width: 100%;
        height: 100%;
        display: flex;
        overflow: hidden;
        backdrop-filter: blur(5px);
        background: rgba(255, 255, 255, 0.2);
        box-shadow: 0px 20px 90px rgba(0, 0, 0, 0.2);
        #Filtro-inputs {
            padding-left: 20px;
            margin-bottom: 5px;
        }
        #Filtro-button {
            #Button {
                width: 100%;
                height: 50px;
                color: black;
                margin-bottom: 20px;
                background-color: rgb(255, 255, 255);
            }
            #Button:hover {
                color: red;
            }
        }
        #Filtro-tittle {
            padding-top: 30px;
            text-align: center;
        }
        #Filtro-tittle:hover {
            cursor: pointer;
        }
        #Divisor-content {
            height: 100%;
            padding-top: 5px;
            padding-bottom: 5px;
            #Filtro-divisores {
                border: 1px solid rgba(255, 0, 0, 0.158);
            }
        }
    }
</style>

<script>
    export default {
        name: "PrecioCell",
        methods: {
            FiltroIntervalo(){
                this.$emit("FiltroIntervalo",this.IntervaloInicial, this.IntervaloFinal);
            },
            Filtro500(){
                this.$emit("Filtro500");
            },
            FiltroReiniciar(){
                this.$emit("FiltroReiniciar");
            },
        },
    };
</script>