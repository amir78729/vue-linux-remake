<template>
  <div style="    border-bottom:5px solid rgb(242,169,56);">

<!--    <h1>{{items}}</h1>-->

    <h2 style="cursor: default">کارگاه‌ها و سخنرانی‌ها</h2>
    <div class="row align-content-center" style="padding: 0 80px 0 80px; justify-content: center">
      <div class="col-md-6 col-sm-12" v-for="item in items">
        <grid-workshop-item
        :title="item.title"
        :imageURL="item.imageURL"
        :teachers="item.teacher"></grid-workshop-item>
      </div>
    </div>
  </div>
</template>
<script>
  import WorkshopItem from "./WorkshopItem.vue";
  import data from "./../data/data.js"

  export default {
    components: {
      gridWorkshopItem: WorkshopItem,
    },
    data() {
      return {

      }
    },
    props: ['items']
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
