<template>
  <div>
<!--    <app-header></app-header>-->
<!--    <app-event-title></app-event-title>-->
<!--    <app-about-event></app-about-event>-->
    <app-workshop-grid></app-workshop-grid>
  </div>
</template>

<script>
  import Header from "./components/Header.vue";
  import EventTitle from "./components/EventTitle.vue";
  import AboutEvent from "./components/AboutEvent.vue";
  import WorkshopGrid from "./components/WorkshopGrid.vue"

  export default {
    components: {
      appHeader: Header,
      appEventTitle: EventTitle,
      appAboutEvent: AboutEvent,
      appWorkshopGrid: WorkshopGrid,
    }
}
</script>

<style>
  body {
    font-family: 'iransans';
  }
</style>
