<template>
<q-page class="flex flex-center">
    <div class="full-width column wrap justify-center items-center content-center">
      <div class="q-px-xl text-center">
        <span>“Usa tus sentidos para entender como te ves y como ves al mundo que te rodea.”</span>
      </div>
      <div style="margin-left: 265px;">
        <span>Ajna</span>
      </div>
    </div>
    <div class="q-mt-xl-xl">
      <ButtonSeeMore :ancle="{hash: '#fabrication-process'}" @action="anchorHashCheck"></ButtonSeeMore>
    </div>
</q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  components: {
    ButtonSeeMore: () => import('src/components/ButtonSeeMore'),
  },
  mounted() {},
  methods: {
    async anchorHashCheck() {
      try {
        setTimeout(() => {
          if (window.location.hash === this.$route.hash) {
            document.getElementById(this.$route.hash.slice(1)).scrollIntoView({
              behavior: 'smooth'
            });
          }
        } , 1000);
      }catch (e) {}
    },
  }
}
</script>

<style scoped>
</style>
