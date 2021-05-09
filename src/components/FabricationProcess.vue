<template>
  <q-page>
    <div class="text-center" style="background: #634624">
      <div><span style="font-size: 35px!important;font-weight: bold;">Proceso de fabricación</span></div>
      <div class="full-width column">
        <div class="row-fabrication"><span>Recepción de Materiales</span></div>
        <div class="row-fabrication"><span>Desinfección de Frutas</span></div>
        <div class="row-fabrication"><span>Pelado y rayado de Frutas</span></div>
        <div class="row-fabrication"><span>Primera maceración con ron</span></div>
        <div class="row-fabrication"><span>Segunda maceración con almibar</span></div>
        <div class="row-fabrication"><span>Filtrado</span></div>
        <div class="row-fabrication"><span>Embotellado y etiquetado</span></div>
        <ButtonSeeMore></ButtonSeeMore>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "FabricationProcess",
  components:{
    ButtonSeeMore: ()=> import('src/components/ButtonSeeMore')
  }
}
</script>

<style scoped>
  *{
   clear: both;
  }
  .row-fabrication{
    margin-bottom: 36px;
    margin-top: 35px;
  }
</style>
