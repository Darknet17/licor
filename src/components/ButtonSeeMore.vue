<template>
  <div class="text-center">
    <div class="justify-center content-center">
      <div>
        <div>
          <q-btn rounded class="see-more" label="Ver mas..." />
        </div>
        <div>
          <q-icon class="expand-more" name="expand_more" size="md" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ButtonSeeMore"
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
