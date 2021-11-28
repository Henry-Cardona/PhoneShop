
<template>
    <div id="Container-producto">
        <v-col cols="12" sm="12" md="6" lg="3">
            <div id="Card" class="rounded-lg">
                <div id="Card-content" class="rounded-lg">
                    <div id="Card-footer" class="rounded-lg">
                        <div id="Card-footer-content" class="rounded-t-xl">
                            <div id="Card-footer-info" class="rounded-xl">
                                <h1 id="Personal-title" class="subtitle-2">Datos del vendedor</h1>
                                <div id="Divisor-content">
                                    <v-divider id="Filtro-divisores"></v-divider>
                                </div>
                                <div id="Personal-info">
                                    <i class='bx bxs-group bx-flashing bx-sm'></i>
                                    <h1 class="subtitle-2">Adelina Martínez</h1>
                                </div>
                                <div id="Personal-info">
                                    <i class='bx bxl-whatsapp bx-flashing bx-sm'></i>
                                    <h1 class="subtitle-2">4652-4521</h1>
                                </div>
                                <div id="Personal-info">
                                    <i class='bx bxl-google bx-flashing bx-sm'></i>
                                    <h1 class="subtitle-2">adelinam26@gmail.com</h1>
                                </div>
                                <div id="Divisor-content">
                                    <v-divider id="Filtro-divisores"></v-divider>
                                </div>
                                <div id="Personal-redes">
                                    <h1 id="Personal-title" class="subtitle-2">Redes sociales</h1>
                                    <i class='bx bxl-facebook bx-flashing bx-sm'></i>
                                    <i class='bx bxl-instagram bx-flashing bx-sm'></i>
                                    <i class='bx bxl-twitter bx-flashing bx-sm'></i>
                                    <i class='bx bxl-snapchat bx-flashing bx-sm'></i>
                                    <i class='bx bxl-tiktok bx-flashing bx-sm'></i>
                                </div>
                            </div>
                        </div>
                    </div>
                    <img id="Img-cell" class="rounded-lg"
                        src="https://image.freepik.com/foto-gratis/emociones-personas-estilo-vida-concepto-moda-entusiasta-mujer-bastante-coreana-traje-elegante-apuntando-esquina-superior-izquierda-mostrando-publicidad-genial-oferta-descuento-especial-fondo-amarillo_1258-58861.jpg" 
                        alt="Celular"
                        >
                </div>
            </div>
        </v-col>
        <v-col id="Carousel-cel" cols="12" sm="12" md="6" lg="3">
            <v-carousel 
                class="rounded-lg" 
                hide-delimiters>
                <v-carousel-item
                    v-for="(item,i) in items"
                    :key="i"
                    :src="item.src"
                ></v-carousel-item>
            </v-carousel>
        </v-col>
        <v-col id="Information" cols="12" sm="12" md="6" lg="6">
            <div id="Information-cel">
                <h1 id="Information-left" class="subtitle-1 d-none d-sm-flex">Marca:</h1>
                <h1 id="Information-right" class="subtitle-1 rounded-lg">Huawei</h1>
            </div>
            <div id="Information-cel">
                <h1 id="Information-left" class="subtitle-1 d-none d-sm-flex">Modelo:</h1>
                <h1 id="Information-right" class="subtitle-1 rounded-lg">Huawei Y6 2019</h1>
            </div>
            <div id="Information-cel">
                <h1 id="Information-left" class="subtitle-1 d-none d-sm-flex">RAM:</h1>
                <h1 id="Information-right" class="subtitle-1 rounded-lg">4 GB</h1>
            </div>
            <div id="Information-cel">
                <h1 id="Information-left" class="subtitle-1 d-none d-sm-flex">Precio:</h1>
                <h1 id="Information-right" class="subtitle-1 rounded-lg">$ 958 USD</h1>
            </div>
            <div id="Information-cel">
                <h1 id="Information-left" class="subtitle-1 d-none d-sm-flex">Descripción:</h1>
                <h1 id="Information-right" class="subtitle-1 rounded-lg">
                    Lorem Ipsum es simplemente texto de relleno de la industria de la impresión y la composición tipográfica. 
                    Lorem Ipsum ha sido el texto de relleno estándar de la industria desde la década de 1500, cuando un impresor 
                    desconocido tomó una galera de tipos y la mezcló para hacer un libro de muestras tipográficas.
                </h1>
            </div>
            <div>
                
            </div>
        </v-col>
    </div>
</template>

<style lang="less" scoped>
    #Container-producto {
        display: flex;
        flex-wrap: wrap;
        #Card {
            width: 100%;
            #Card-content {
                width: 100%;
                height: 500px;
                overflow: hidden;
                position: relative;
                box-shadow: 0px 5px 10px -2px rgba(74, 54, 251, 0.2);
                #Card-footer {
                    overflow: hidden;
                    #Card-footer-content {
                        bottom: 0%;
                        width: 100%;
                        display: flex;
                        padding: 10px;
                        overflow: hidden;
                        position: absolute;
                        align-items: center;
                        backdrop-filter: blur(4px);
                        background: rgba(255, 255, 255, 0.2);
                        box-shadow: 0px 20px 50px rgba(0, 0, 0, 0.2);
                        #Card-footer-info {
                            width: 100%;
                            align-items: center;
                            #Personal-title {
                                width: 100%;
                                height: 35px;
                                padding-top: 5px;
                                text-align: center;
                            }
                            #Personal-info {
                                display: flex;
                                height: 30px;
                                margin-bottom: 10px;
                                h1 {
                                    padding-top: 2px;
                                    padding-left: 10px;
                                }
                                i {
                                    padding-left: 10px;
                                }
                            }
                            #Personal-redes {
                                width: 100%;
                                height: 40px;
                                padding-top: 5px;
                                display: flex;
                                padding-left: 20px;
                                padding-right: 20px;
                                i {
                                    width: 30px;
                                }
                                h1 {
                                    width: 50%;
                                }
                            }
                            #Divisor-content {
                                height: 15px;
                                #Filtro-divisores {
                                    border: 1px solid rgba(184, 174, 174, 0.384);
                                }
                            }
                        }
                    }
                }
                #Img-cell {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                    object-position: center center;
                }
            }
        }
        #Information {
            width: 100%;
            #Information-cel {
                width: 100%;
                display: flex;
                padding-top: 15px;
                #Information-left {
                    width: 20%;
                    padding-right: 15px;
                }
                #Information-right {
                    width: 100%;
                    padding-top: 5px;
                    padding-bottom: 5px;
                    padding-left: 20px;
                    padding-right: 20px;
                    background: rgba(184, 174, 174, 0.247);
                }
            }
        }
    }
</style>

<script>
    export default {
        name: "AnuncioCom",
        data () {
            return {
                items: [
                {
                    src: 'https://i.ytimg.com/vi/wLMrNwA19-Q/maxresdefault.jpg',
                },
                {
                    src: 'https://i.ytimg.com/vi/wLMrNwA19-Q/maxresdefault.jpg',
                },
                {
                    src: 'https://i.ytimg.com/vi/wLMrNwA19-Q/maxresdefault.jpg',
                },
                {
                    src: 'https://i.ytimg.com/vi/wLMrNwA19-Q/maxresdefault.jpg',
                },
                ],
            }
        },
    }
</script>