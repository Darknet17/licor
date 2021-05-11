<template>
  <div style="background: #634624;height: 37px;">
    <div class="fit row wrap justify-between items-center content-center">
        <div>
          <span class="q-ml-md">&copy; Licores Artesanales Ajne {{ getYear() }}</span>
        </div>
        <div>
          <a href="#"><q-icon name="fab fa-whatsapp" class="q-mr-md"></q-icon></a>
          <a href="#"><q-icon name="fab fa-instagram" class="q-mr-md"></q-icon></a>
          <a href="#"><q-icon name="fab fa-facebook" class="q-mr-md"></q-icon></a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  methods:{
    getYear(){
      let date = new Date();
      return date.getFullYear();
    }
  }
}
</script>

<style scoped>

</style>
