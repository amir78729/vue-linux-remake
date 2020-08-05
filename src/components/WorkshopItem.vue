<template>
  <div class="item">
    <h4 style="font-weight: bolder;">{{ title }}</h4>
    <h5 v-for="name in names">{{ name }}</h5>
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
    border-radius: 10px;
    padding: 30px;
  }
  .item:hover {
    background-color: #521C39;
    color: #e4b22b;
    box-shadow: 0 0 5px 0 black;
    border-radius: 15px;
  }
</style>
