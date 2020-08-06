<template>
  <div>
    <app-header style="position: fixed; width: 100%" class="always-on-top"></app-header>
    <app-event-title></app-event-title>
    <app-about-event></app-about-event>
    <app-workshop-grid></app-workshop-grid>
    <app-snapp></app-snapp>
  </div>
</template>

<script>
  import Header from "./components/Header.vue";
  import EventTitle from "./components/EventTitle.vue";
  import AboutEvent from "./components/AboutEvent.vue";
  import WorkshopGrid from "./components/WorkshopGrid.vue";
  import Snapp from "./components/Snapp.vue";


  export default {
    components: {
      appHeader: Header,
      appEventTitle: EventTitle,
      appAboutEvent: AboutEvent,
      appWorkshopGrid: WorkshopGrid,
      appSnapp: Snapp,
    }
}
</script>

<style>
  body {
    font-family: 'iransans';
  }
  .always-on-top {
    z-index: 999999 !important;
  }
</style>
