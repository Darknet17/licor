<template>
<q-page class="flex flex-center">
    <div class="text-center q-my-xl">
      <div class="q-px-xl">
        <span>“Usa tus sentidos para entender como te ves y como ves al mundo que te rodea.”</span>
      </div>
      <div class="row justify-between">
        <div></div>
        <div class="q-mx-xl">
          <span></span>
          <span>Ajna</span>
        </div>
      </div>
    </div>
    <div class="q-mt-xl-xl">
      <ButtonSeeMore></ButtonSeeMore>
    </div>
</q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  components: {
    ButtonSeeMore: () => import('src/components/ButtonSeeMore'),
  }
}
</script>

<style scoped>
</style>
