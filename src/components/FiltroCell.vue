
<template>
    <v-container id="Filtro-content" class="spacing-playground pa-0 rounded-xl" fluid>
        <div id="Filtro-border" class="rounded-lg">
            <h1 id="Filtro-texto" class="subtitle-2">Filtrado</h1>
            <img 
                id="Filtro-img"
                src="https://cdn-icons-png.flaticon.com/512/1923/1923751.png" 
                alt="Filtro de modelo">
            <v-btn id="Button" class="rounded-pill" depressed>
                <i class='bx bx-search bx-flashing bx-sm'></i>
                <h1 id="Texto-button" class="subtitle-2">Buscar</h1>
            </v-btn>
        </div>
        <v-divider id="Filtro-divisores"></v-divider>
        <div id="Filtro-options">
            <h1 id="Texto-options" class="subtitle-2">Nuevo</h1>
            <div id="Switch-options">
                <v-switch
                    color="red"
                    value="red"
                    hide-details
                ></v-switch>
            </div>
        </div>
        <div id="Filtro-options">
            <h1 id="Texto-options" class="subtitle-2">Orden</h1>
            <v-btn @click="OrdenarPrecio" id="Button" class="rounded-pill" depressed>
                <i v-show="Ascendente" class='bx bxs-upvote bx-flashing bx-sm'></i>
                <i v-show="!Ascendente" class='bx bxs-upvote bx-flashing bx-rotate-180 bx-sm'></i>
                <h1 v-show="Ascendente" id="Texto-button" class="subtitle-2">Ascend.</h1>
                <h1 v-show="!Ascendente" id="Texto-button" class="subtitle-2">Descen.</h1>
            </v-btn>
        </div>
        <div id="Filtro-options">
            <h1 id="Texto-options" class="subtitle-2">Marca de celular</h1>
            <div id="Check-options">
                <v-checkbox
                    label="Samsung"
                    color="red"
                    hide-details
                ></v-checkbox>
                <v-checkbox
                    label="Huawei"
                    color="red"
                    hide-details
                ></v-checkbox>
                <v-checkbox
                    label="iPhone"
                    color="red"
                    hide-details
                ></v-checkbox>
                <v-checkbox
                    label="OnePlus"
                    color="red"
                    hide-details
                ></v-checkbox>
                <v-checkbox
                    label="Xiaomi"
                    color="red"
                    hide-details
                ></v-checkbox>
            </div>
        </div>
        <div id="Filtro-options">
            <h1 id="Texto-options" class="subtitle-2">Sistema operativo</h1>
            <div id="Check-options">
                <v-checkbox
                    label="Android"
                    color="red"
                    hide-details
                ></v-checkbox>
                <v-checkbox
                    label="Ios"
                    color="red"
                    hide-details
                ></v-checkbox>
                <v-checkbox
                    label="Windows"
                    color="red"
                    hide-details
                ></v-checkbox>
            </div>
        </div>
    </v-container>
</template>

<style lang="less" scoped>
    #Filtro-content {
        width: 100%;
        height: 100%;
        backdrop-filter: blur(5px);
        background: rgba(255, 255, 255, 0.2);
        box-shadow: 0px 20px 90px rgba(0, 0, 0, 0.2);
        #Filtro-border {
            padding: 15px;
            #Filtro-texto {
                width: 100%;
                height: 45px;
                padding-top: 10px;
                text-align: center;
            }
            #Filtro-img {
                width: 140px;
                height: 140px;
                margin-bottom: 10px;
            }
            #Button {
                width: 100%;
                height: 50px;
                color: black;
                background-color: white;
            }
            #Button:hover {
                color: red;
            }
        }
        #Filtro-divisores {
            border: 1px solid rgba(255, 0, 0, 0.158);
        }
        #Filtro-options {
            width: 100%;
            padding: 15px;
            #Texto-options {
                width: 100%;
                height: 30px;
                padding-top: 10px;
                text-align: center;
            }
            #Button {
                width: 100%;
                height: 50px;
                color: black;
                margin-top: 10px;
                background-color: white;
            }
            #Button:hover {
                color: red;
            }
            #Switch-options {
                width: 100%;
                padding-left: 65px;
            }
        }
    }
</style>

<script>
    export default {
        name: "FiltroCell",
        data: () => ({
            items: ['Todos','Huawei', 'Samsung', 'Apple', 'Sony', 'Xiaomi', 'LG','OnePlus'],
            value: ['Todos'],
            Ascendente: true,
        }),
        methods: {
            OrdenarPrecio(){
                this.Ascendente=!this.Ascendente;
                this.$emit("OrdenarPrecio",this.Ascendente);
            }
        },
    };
</script>