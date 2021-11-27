<template>
  <v-container>
    <NavBar/>
    <v-row id="Page-content">
      <v-col md="3" lg="2" class="d-none d-sm-flex">
        <FiltroCell @OrdenarPrecio="OrdenarPrecio"/>
      </v-col>
      <v-col xs="12" lg="10" id="Page-cards">
        <div id="Filtro-precio" class="">
          <PrecioCell @FiltroIntervalo="FiltroIntervalo" @Filtro500='Filtro500' @FiltroReiniciar='FiltroReiniciar'/>
        </div>
        <v-row>
          <v-col id="Tabla-cell">
            <CellAnun ref="anuncios1"/>
          </v-col>
        </v-row>
      </v-col>
      <FooterCell id="Footer"/>
    </v-row>
  </v-container>
</template>

<style lang="less" scoped>
  #Page-content {
    #Page-cards {
      display: grid;
      #Filtro-precio {
        padding-top: 10px;
        padding-left: 20px;
      }
      #Tabla-cell {
        display: contents;
        padding-top: 80px;
      }
    }
  }
  #Footer {
    width: 100%;
  }
</style>

<script>
  import CellAnun from '../components/CellAnun.vue'
  import NavBar from '../components/NavBar.vue'
  import FooterCell from '../components/FooterCell.vue'
  import FiltroCell from '../components/FiltroCell'
  import PrecioCell from '../components/PrecioCell.vue'
  export default {
    name: 'Home',
    components: {
      CellAnun,
      FiltroCell,
      PrecioCell,
      NavBar,
      FooterCell,
    },
    methods: {
      OrdenarPrecio(Ascendente){
        this.$refs.anuncios1.OrdenarPrecio(Ascendente);
      },
      FiltroIntervalo(IntervaloInicial, IntervaloFinal){
        this.$refs.anuncios1.FiltroIntervalo(IntervaloInicial, IntervaloFinal);
      },
      Filtro500(){
        this.$refs.anuncios1.Filtro500();
      },
      FiltroReiniciar(){
        this.$refs.anuncios1.FiltroReiniciar();
      }
    },
  }
</script>
