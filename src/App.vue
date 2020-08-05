<template>
  <div>
    <app-header></app-header>
    <app-event-title></app-event-title>
    <app-about-event></app-about-event>
  </div>
</template>

<script>
  import Header from "./components/Header.vue";
  import EventTitle from "./components/EventTitle.vue";
  import AboutEvent from "./components/AboutEvent.vue";

  export default {
    components: {
      appHeader: Header,
      appEventTitle: EventTitle,
      appAboutEvent: AboutEvent,

    }
}
</script>

<style>
  body {
    font-family: 'iransans';
  }
</style>
