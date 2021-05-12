<template>
  <div style="background: #634624;height: 37px;">
    <div class="fit row wrap justify-between items-center content-center">
        <div>
          <span class="q-ml-md">&copy; Licores Artesanales Ajne {{ getYear() }}</span>
        </div>
        <div>
          <a href="https://api.whatsapp.com/send?phone=809000000" target="_blank"><q-icon name="fab fa-whatsapp" class="q-mr-md"></q-icon></a>
          <a href="https://www.instagram.com/" target="_blank"><q-icon name="fab fa-instagram" class="q-mr-md"></q-icon></a>
          <a href="https://www.facebook.com/" target="_blank"><q-icon name="fab fa-facebook" class="q-mr-md"></q-icon></a>
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
  a {
    text-decoration: none;
  }
</style>
