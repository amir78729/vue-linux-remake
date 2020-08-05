<template>
  <div>
    <app-header></app-header>
    <app-event-title></app-event-title>
  </div>
</template>

<script>
  import Header from "./components/Header.vue";
  import EventTitle from "./components/EventTitle.vue"

  export default {
    components: {
      appHeader: Header,
      appEventTitle: EventTitle
    }
}
</script>

<style>
  body {
    font-family: 'iransans';
  }
</style>
