<template>
  <div>
    <h2>کارگاه‌ها و سخنرانی‌ها</h2>
    <div class="row align-content-center" style="padding: 0 20px 0 20px">
      <div class="col-md-6 col-sm-12">
        <grid-workshop-item></grid-workshop-item>
      </div>
      <div class="col-md-6 col-sm-12">
        <grid-workshop-item ></grid-workshop-item>
      </div>
    </div>
  </div>
</template>
<script>
  import WorkshopItem from "./WorkshopItem.vue";

  export default {
    components: {
      gridWorkshopItem: WorkshopItem,
    }
  }
</script>
<style scoped>
  h2 {
    margin: 50px;
    font-size: 36px;
    color: #521C39;
    text-align: center;
    font-weight: bolder;
  }
</style>
