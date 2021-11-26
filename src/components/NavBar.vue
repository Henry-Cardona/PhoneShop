
<template>
    <v-bar id="NavBar">
        <v-app-bar id="NavBar-container"
            app
            dark
            color= white>
            <v-row id="NavBar-content">
                <v-col id="NavBar-img" cols="2">
                    <i class='bx bxs-store bx-md'></i>
                    <h1 id="NavBar-name" class="subtitle-2 d-none d-sm-flex">Phone shop CV19014</h1>
                </v-col>
                <v-col id="NavBar-search" cols="4" class="d-none d-sm-flex">
                    <div id="Input">
                        <input type="text" placeholder="  ¿Qué estás buscando?">
                        <i class='bx-sm bx bx-search-alt'></i>
                    </div>
                </v-col>
                <div id="NavBar-button" cols="6">
                    <div id="NavBar-button-content">
                        <v-btn id="Button" class="rounded-pill" depressed>
                            <i class='bx bx-current-location bx-flashing bx-sm d-none d-sm-flex'></i>
                            <h1 id="Texto-button" class="subtitle-2">Inicio</h1>
                        </v-btn>
                    </div>
                    <div id="NavBar-button-content" class="d-none d-sm-flex">
                        <v-btn id="Button" class="rounded-pill" depressed>
                            <i class='bx bx-stats bx-flashing bx-sm'></i>
                            <h1 id="Texto-button" class="subtitle-2">Estadística</h1>
                        </v-btn>
                    </div>
                    <div id="NavBar-button-content">
                        <v-dialog
                            v-model="dialog"
                            fullscreen
                            hide-overlay
                            transition="dialog-bottom-transition">
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn v-bind="attrs" v-on="on" id="Button" class="rounded-pill" depressed>
                                    <i class='bx bxs-add-to-queue bx-flashing bx-sm d-none d-sm-flex'></i>
                                    <h1 id="Texto-button" class="subtitle-2">Anuncio</h1>
                                </v-btn>
                            </template>
                            <v-card>
                                <v-toolbar></v-toolbar>
                                <v-toolbar dark color="rgba(255, 0, 0, 0.733)" class="rounded-b-xl">
                                    <v-btn icon dark @click="dialog = false">
                                        <v-icon color="black">mdi-close</v-icon>
                                    </v-btn>
                                    <v-toolbar-title>Publicar nuevo anuncio</v-toolbar-title>
                                </v-toolbar>
                                <NewCell/>
                                <v-footer dark color="rgba(255, 0, 0, 0.733)" class="rounded-t-xl">Nuevo anuncio</v-footer>
                            </v-card>
                        </v-dialog>
                    </div>
                    <div id="NavBar-button-content" class="d-none d-sm-flex">
                        <v-btn id="Button" class="rounded-pill" depressed>
                            <i class='bx bxs-badge-dollar bx-flashing bx-sm'></i>
                            <h1 id="Texto-button" class="subtitle-2">Ofertas</h1>
                        </v-btn>
                    </div>
                    <div id="NavBar-button-content">
                        <v-btn id="Button" class="rounded-pill" depressed>
                            <i class='bx bxs-shopping-bag bx-flashing bx-sm d-none d-sm-flex'></i>
                            <h1 id="Texto-button" class="subtitle-2">Compras</h1>
                        </v-btn>
                    </div>
                </div>
            </v-row>
        </v-app-bar>
    </v-bar>
</template>

<style lang="less" scoped>
    #NavBar {
        z-index: 4000;
        position: fixed;
        #NavBar-container {
            height: 100%;
            #NavBar-content {
                height: 100%;
                #NavBar-button {
                    width: 45%;
                    height: 100%;
                    padding: none;
                    display: flex;
                    #NavBar-button-content {
                        width: 100%;
                        height: 100%;
                        #Button {
                            width: 100%;
                            height: 100%;
                            color: black;
                            background-color: white;
                            #Texto-button {
                                padding-left: 5px;
                            }
                        }
                        #Button:hover {
                            color: red;
                        }
                    }
                }
                #NavBar-search {
                    #Input{
                        width: 100%;
                        height: 100%;
                        display: flex;
                        position: relative;
                        align-items: center;
                        i {
                            right: 0;
                            color: black;
                            font-size: 1rem;
                            position: absolute;
                            margin-right: 10px;
                        }
                        input {
                            height: 100%;
                            width: 100%;
                            border: none;
                            outline: none;
                            padding: 10px;
                            border-radius: 20px;
                            background-color: rgba(255, 0, 0, 0.733);
                        }
                    }
                }
                #NavBar-img {
                    height: 100%;
                    color: black;
                    display: flex;
                    align-items: center;
                    #NavBar-name {
                        width: 100%;
                        padding-left: 10px;
                    }
                }
            }
        }
    }
</style>

<script>
    import NewCell from "./NewCell.vue";
    export default {
        name: "NavBar",
        components: {
            NewCell,
        },
        data() {
            return {
                dialog: false,
            }
        },
    };
</script>