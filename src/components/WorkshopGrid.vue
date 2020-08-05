<template>
  <div>
    <h2>کارگاه‌ها و سخنرانی‌ها</h2>
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
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'Kernel',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'Penetration Testing with Kali Linux',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'Virtualization',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'Container Orchestration in Cloud',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'اسنپ‌کلود:‌ دلایل بنیادین و نحوه ساخت',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
          },
          {
            title: 'Service Discovery',
            names: ['علیرضا بختیاری','شایان شقفی','محمد فاطمی']
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
