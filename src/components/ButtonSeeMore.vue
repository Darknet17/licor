<template>
  <div class="text-center q-mt-xl-xl">
    <div class="justify-center content-center">
      <div>
        <div>
          <q-btn rounded class="see-more" label="Ver mas..." @click="action" />
        </div>
        <div>
          <q-icon class="expand-more slide-bottom" name="expand_more" size="md" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ButtonSeeMore",
  methods: {
    action(){
      this.$emit('action');
    }
  }
}
</script>

<style scoped>
  .see-more{
    background-color: #894819;
    width: 187px!important;
    height: 44px!important;
    font-size: 18px!important;
  }
  .expand-more{
    color: #894819;
  }
</style>
