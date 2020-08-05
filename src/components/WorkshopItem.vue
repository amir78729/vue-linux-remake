<template>
  <div dir="rtl" class="row item">
    <div class="col-xl-5 col-lg-5 col-md-4 col-sm-6 col-xs-6 bg-info item-img">
    </div>
    <div class="col-xl-7 col-lg-7 col-md-8 col-sm-6 col-xs-6 item-text">
      <h4 style="font-weight: bolder;">{{ title }}</h4>
      <h5 v-for="name in names">{{ name }}</h5>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'عنوان',
        names: ['name1', 'name2', 'name3']
      }
    },
  }
</script>

<style>
  .item {
    background-color: #292929;
    color: white;
    transition: all 0.3s;
    border-radius: 20px;
    margin: 10px 10px 30px 10px;
  }
  .item:hover {
    background-color: #521C39;
    color: #e4b22b;
    box-shadow: 0 0 5px 0 black;
    border-radius: 10px;
  }
  .item:hover .item-img {
    border-radius: 0px 10px 10px 0px;
    transition: all 0.3s;
    border-left: solid 2px #e4b22b;
  }
  .item-text {
    padding: 30px;
    text-align: right;
  }
  .item-img {
    border-radius: 0px 20px 20px 0px;
    transition: all 0.3s;
    border-left: solid 2px white;
  }
  .item-img:hover {
    filter: brightness(0.8);
  }

</style>
