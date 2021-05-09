<template>
  <div style="background: #634624;height: 37px;">
    <div class="row justify-between items-center">
      <div>
        <div>
          &copy; Licores Artesanales Ajne {{ getYear() }}
        </div>
        <div></div>
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
