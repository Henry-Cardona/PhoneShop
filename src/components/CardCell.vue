
<template>
    <v-col cols="12" sm="12" md="6" lg="4">
        <div id="Card" class="rounded-xl">
            <div id="Card-content" class="rounded-xl">
                <div id="Card-brand" class="rounded-xl">
                    <i class='bx bx-check bx-flashing bx-sm' ></i>
                    <h1 class="subtitle-1">{{cv19014Productos.Estado}}</h1>
                </div>
                <div id="Card-footer" class="rounded-xl">
                    <div id="Card-footer-content" class="rounded-xl">
                        <div id="Card-footer-left" class="rounded-xl">
                            <div id="Title">
                                <i class='bx bx-badge-check bx-flashing bx-sm'></i>
                                <h1 class="subtitle-2">{{cv19014Productos.Modelo}}</h1>
                            </div>
                            <div id="User">
                                <div id="User-content">
                                    <div id="User-img" class="rounded-circle">
                                        <img 
                                            src="https://image.freepik.com/free-photo/positive-attractive-girl-taking-selfie-showing-v-sign-peace-gesture-near-eye-holding-camera-with-stretched-hand-making-photo-smartphone-white-wall_176420-39446.jpg" 
                                            alt="User image"
                                            id="Img"
                                        />
                                    </div>
                                    <div id="User-name">
                                        <h1 class="subtitle-2">{{cv19014Productos.Vendedor}}</h1>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div id="Card-footer-right" class="rounded-xl">
                            <div id="Price">
                                <h1 class="subtitle-1">$ {{cv19014Productos.Precio}} USD</h1>
                            </div>
                            <div id="Icon-cel">
                                <div id="Icon-coments">
                                    <i class='bx bxs-check-circle bx-sm' ></i>
                                    <i class='bx bxs-x-circle bx-sm' ></i>
                                    <i class='bx bxl-telegram bx-sm'></i>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div id="Card-footer-link">
                        <button class="rounded-xl">
                            <slot>
                                <h1 class="subtitle-1">Ver más detalles</h1>
                            </slot>
                        </button>
                    </div>
                </div>
                <img id="Img-cell" class="rounded-xl"
                    :src="cv19014Productos.ImagenCel" 
                    alt="Celular"
                    >
            </div>
        </div>
    </v-col>
</template>

<style lang="less" scoped>
    #Card {
        width: 100%;
        #Card-content {
            width: 100%;
            height: 500px;
            overflow: hidden;
            position: relative;
            box-shadow: 0px 5px 10px -2px rgba(74, 54, 251, 0.2);
            #Card-brand {
                top: 0;
                padding: 5px;
                margin: 20px;
                color: white;
                display: flex;
                font-size: 0.9rem;
                position: absolute;
                backdrop-filter: blur(5px);
                background: rgba(255, 255, 255, 0.2);
                box-shadow: 0px 20px 50px rgba(0, 0, 0, 0.2);
                i {
                    width: 25px;
                    height: 25px;
                }
                h1 {
                    padding-left: 3px;
                    padding-right: 5px;
                }
            }
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
                    #Card-footer-left {
                        width: 60%;
                        #Title {
                            height: 50px;
                            display: flex;
                            align-items: center;
                            i {
                                width: 35%;
                                padding-right: 5px;
                                color: white;
                                text-align: end;
                            }
                            h1 {
                                width: 100%;
                                color: white;
                                padding: 5px;
                                text-align: initial;
                            }
                        }
                        #User {
                            height: 120px;
                            display: flex;
                            flex-direction: column;
                            #User-content {
                                display: flex;
                                margin-left: 10px;
                                align-items: center;
                                #User-img{
                                    width: 40px;
                                    height: 40px;
                                    overflow: hidden;
                                    #Img {
                                        width: 100%;
                                        height: 100%;
                                        object-fit: cover;
                                        object-position: center center;
                                    }
                                }
                                #User-name {
                                    color: white;
                                    margin-left: 10px;
                                }
                            }
                        }
                    }
                    #Card-footer-right {
                        width: 40%;
                        height: 170px;
                        padding: 10px;
                        align-items: center;
                        #Price {
                            height: 50px;
                            color: white;
                            align-items: center;
                            h1 {
                                text-align: center;
                            }
                        }
                        #Icon-cel {
                            width: 100%;
                            color: white;
                            #Icon-coments {
                                padding-left: 3px;
                                justify-content: space-evenly;
                                i {
                                    padding-left: 2px;
                                    padding-right: 3px;
                                }
                            }
                        }
                    }
                }
                #Card-footer-link {
                    bottom: 0%;
                    width: 95%;
                    padding: 10px;
                    margin-left: 5px;
                    margin-right: 5px;
                    overflow: hidden;
                    position: absolute;
                    align-items: center;
                    border-top: 1px solid white;
                    button {
                        width: 100%;
                        border: none;
                        color: white;
                        outline: none;
                        padding: 10px 10px;
                        background-color: rgba(255, 0, 0, 0.733);
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
</style>

<script>
    export default {
        name: "CardCell",
        props : ["cv19014Productos"]
        
    };
</script>
