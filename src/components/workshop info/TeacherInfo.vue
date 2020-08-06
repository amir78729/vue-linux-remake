<template>
  <div style="justify-items: center;" class=" bg-warning">
    <div class="pic"></div>
    <h3 class="teacher-title">{{teachers[index].teacherName}}</h3>
    <h4 class="teacher-info">{{ teachers[index].teacherInfo }}</h4>
  </div>
</template>
<script>
  export default {
    props:['teachers', 'index']
  }
</script>
<style>
  .pic {
    justify-content: center;
    height: 150px;
    width: 150px;
    border-radius: 75px;
    background-color: #292929;

  }
  .teacher-title {
    font-size: 24px;
    text-align: center;
  }
  .teacher-info {
    font-size: 18px;
    width: 200px;
    text-align: center;
  }
</style>
