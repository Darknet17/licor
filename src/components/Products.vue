<template>
  <q-page class="flex flex-center">
    <div style="background: #f9eadc;" id="productos">
      <div class="text-center"><span style="color:#894819; font-size: 35px; font-weight: bold;">Productos</span></div>
      <div class="row justify-between">
        <div><img class="product" src="../assets/img/Artboard-1xxx-hdpi.png" alt="Artboard-1xxx-hdpi"></div>
        <div><img class="product" src="../assets/img/Artboard-3xxxhdpi.png" alt="Artboard-3xxxhdpi"></div>
        <div><img class="product" src="../assets/img/Artboard-4xxxhdpi.png" alt="Artboard-4xxxhdpi"></div>
        <div><img class="product" src="../assets/img/Artboard-5xxxhdpi.png" alt="Artboard-5xxxhdpi"></div>
      </div>
      <div class="text-center">
        <div>
          <q-btn flat rounded style="color: #894819; font-size: 18px; font-weight: bold;" label="Ver mas.." />
        </div>
        <div>
          <q-icon class="expand-more slide-bottom" style="color: #894819; font-weight: bold;" name="expand_more" size="md" />
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "Products",
  methods: {
    anchorHashCheck() {
      try {
        setTimeout(() => {
          if (window.location.hash === this.$route.hash) {
            console.log('Products');
            document.getElementById(this.$route.hash.slice(1)).scrollIntoView({
              behavior: 'smooth'
            });
          }
        } , 1000);
      }catch (e) {}
    },
  },
  mounted() {
    //this.anchorHashCheck()
  },
}
</script>

<style scoped>
  .product{
    width: 188px;
    height: 375px;
  }
</style>
