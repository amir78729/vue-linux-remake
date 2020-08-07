<template>
  <div>
    <app-event-title></app-event-title>
    <app-about-event></app-about-event>
    <app-workshop-grid :items="data"></app-workshop-grid>
    <app-snapp></app-snapp>
  </div>
</template>

<script>
  import EventTitle from "./../home/EventTitle.vue";
  import AboutEvent from "./../home/AboutEvent.vue";
  import WorkshopGrid from "./../home/WorkshopGrid.vue";
  import Snapp from "./../home/Snapp.vue";
  import WorkshopComponent from "./../workshop info/WorkshopComponent.vue"
  export default {
    props: ['data'],
    components: {
      appEventTitle: EventTitle,
      appAboutEvent: AboutEvent,
      appWorkshopGrid: WorkshopGrid,
      appSnapp: Snapp,
      appWorkshopComponent: WorkshopComponent,
    },
  }
</script>

<style>

</style>
