<template>
  <div style="    border-bottom:5px solid rgb(242,169,56);">
    <h2 style="cursor: default">کارگاه‌ها و سخنرانی‌ها</h2>
    <div class="row align-content-center" style="padding: 0 80px 0 80px">
      <div class="col-md-6 col-sm-12" v-for="(item, index) in items">
        <grid-workshop-item
        :title="item.title"
        :names="item.names"></grid-workshop-item>
      </div>
<!--      <div class="col-md-6 col-sm-12">-->
<!--        <grid-workshop-item ></grid-workshop-item>-->
<!--      </div>-->
<!--      <div class="col-md-6 col-sm-12">-->
<!--        <grid-workshop-item></grid-workshop-item>-->
<!--      </div>-->
<!--      <div class="col-md-6 col-sm-12">-->
<!--        <grid-workshop-item ></grid-workshop-item>-->
<!--      </div>-->
    </div>
  </div>
</template>
<script>
  import WorkshopItem from "./WorkshopItem.vue";

  export default {
    components: {
      gridWorkshopItem: WorkshopItem,
    },
    data() {
      return {
        items: [
          {
            title: 'مقدماتی',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'Docker',
            names: ['احمد انواری']
          },
          {
            title: 'Cloud: A solution to infrastructure problem',
            names: ['محمد کریمی']
          },
          {
            title: 'Kernel',
            names: ['بهادر بخشی']
          },
          {
            title: 'Penetration Testing with Kali Linux',
            names: ['احسان عدالت']
          },
          {
            title: 'Virtualization',
            names: ['پرهام الوانی']
          },
          {
            title: 'Container Orchestration in Cloud',
            names: ['امید رجب‌آقا']
          },
          {
            title: 'اسنپ‌کلود:‌ دلایل بنیادین و نحوه ساخت',
            names: ['حسین مرادقلی']
          },
          {
            title: 'Service Discovery',
            names: ['محمد عبدلی‌راد','نرگس احمدی']
          },
        ]
      }
    },
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
