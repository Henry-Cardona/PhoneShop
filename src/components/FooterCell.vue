
<template>
    <v-footer id="Footer" class="rounded-t-lg">
            <v-col id="Footer-info" cols="12" lg="3">
                <h1 class="subtitle-2">Elaborado por:</h1>
                <div id="Personal-info">
                    <i class='bx bxs-user bx-flashing bx-sm'></i>
                    <h1 class="subtitle-2">Henry Rolando Cardona Valle</h1>
                </div>
                <div id="Personal-info">
                    <i class='bx bxs-analyse bx-flashing bx-sm'></i>
                    <h1 class="subtitle-2">CV19014</h1>
                </div>
                <div id="Personal-info">
                    <i class='bx bxs-institution bx-flashing bx-sm'></i>
                    <h1 class="subtitle-2">Universidad de El Salvador</h1>
                </div>
            </v-col>
            <v-col id="Footer-info" cols="12" lg="6">
                <h1 class="subtitle-2">Objetivo del proyecto</h1>
                <p class="subtitle-2">
                    Proyecto desarrollado con el FrameWork Vue, la librería de Vuetify y una conexión con Firebase, 
                    en el que simulamos una página de venta de celulares con distintas funciones como comprar, crear 
                    y ver estadísticas de los productos para la materia de Fundamentos de programación en internet.</p>
            </v-col>
            <v-col id="Footer-info" cols="12" lg="3">
                <h1 class="subtitle-2">Tecnologías utilizadas</h1>
                <div id="Tecnologias-info">
                    <i class='bx bxl-vuejs bx-flashing bx-md'></i>
                    <i class='bx bxl-nodejs bx-flashing bx-md'></i>
                    <i class='bx bxl-javascript bx-flashing bx-md'></i>
                    <i class='bx bxl-html5 bx-flashing bx-md'></i>
                    <i class='bx bxl-firebase bx-flashing bx-md'></i>
                </div>
                <div id="Tecnologias-info">
                    <i class='bx bxl-less bx-flashing bx-md'></i>
                    <i class='bx bxl-css3 bx-flashing bx-md'></i>
                    <i class='bx bxl-github bx-flashing bx-md'></i>
                    <i class='bx bxl-visual-studio bx-flashing bx-md'></i>
                    <i class='bx bxl-git bx-flashing bx-md'></i>
                </div>
            </v-col>
    </v-footer>
</template>

<style lang="less" scoped>
    #Footer {
        height: 100%;
        display: flex;
        flex-wrap: wrap;
        position: relative;
        align-items: center;
        background-color: rgba(255, 0, 0, 0.733);
        #Footer-info {
            width: 100%;
            justify-content: space-between;
            h1 {
                height: 40px;
                text-align: center;
            }
            #Personal-info {
                width: 100%;
                height: 30px;
                display: flex;
                i {
                    padding-right: 10px;
                }
            }
            #Tecnologias-info {
                padding-top: 10px;
                align-items: center;
                width: 100%;
                justify-content: center;
                i {
                    padding-left: 15px;
                }
                i:hover {
                    color: red;
                }
            }
        }
    }
</style>

<script>
    export default {
        name: "FooterCell",
    }
</script>