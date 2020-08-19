<template>
  <div>
    <app-header style="position: fixed; width: 100%" class="always-on-top"></app-header>
    <transition name="fade-slow" mode="out-in">
      <app-home
        :data="items"
        @setIndex="setWorkshopIndex($event)"
        v-if="isHome"></app-home>
      <app-workshop-component
        :data="items"
        :workshop-index="currentWorkshopIndex"
        :selected-workshop="items[currentWorkshopIndex]"
        v-else
        @goBack="isHome = true"></app-workshop-component>
    </transition>
    <app-footer></app-footer>
  </div>
</template>

<script>
  import Header from "./components/Header.vue";
  import WorkshopComponent from "./components/workshop info/WorkshopComponent.vue"
  import Footer from "./components/Footer.vue"
  import { data } from "./data/data";
  import Home from "./components/home/Home.vue";
  import index from "./router";

  export default {

    components: {
      appHeader: Header,
      appWorkshopComponent: WorkshopComponent,
      appHome: Home,
      appFooter: Footer,
    },
    data() {
      return {
        isHome: true,
        currentWorkshopIndex: 1,
        items: data
      }
    },
    methods: {
      setWorkshopIndex(index){
        this.currentWorkshopIndex = index;
        this.isHome = false;
      }
    }
}
</script>

<style>
  body {
    font-family: 'iransans';
    /*background-color: #191919;*/
  }
  .always-on-top {
    z-index: 999999 !important;
  }


  .fade-slow-enter {
    opacity: 0;
  }
  .fade-slow-enter-active {
    animation: slide-in .5s ease-out;
    transition: opacity .5s;
  }
  .fade-slow-leave {

  }
  .fade-slow-leave-active {
    animation: slide-out .5s ease-out;
    transition: opacity .5s;
    opacity: 0;
  }
  @keyframes slide-in {
    from{
      transform: translateX(-20px);
    }
    to{
      transform: translateX(0);
    }
  }
  @keyframes slide-out {
    from{
      transform: translateX(0px);
    }
    to{
      transform: translateX(20px);
    }
  }

</style>
