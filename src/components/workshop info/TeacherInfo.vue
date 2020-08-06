<template>
  <div style="position: relative" class="information ">
    <div class="container">
      <div class="pic align-content-center" :style="{backgroundImage: `url(${teachers[index].teacherImageURL})`}"></div>
      <h3 class="teacher-title">{{teachers[index].teacherName}}</h3>
      <h4 class="teacher-info">{{ teachers[index].teacherInfo }}</h4>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        name: '',
        info:''
      }
    },
    props:['teachers', 'index']
  }
</script>
<style>
  .pic {
    justify-content: center;
    height: 150px;
    width: 150px;
    border-radius: 75px;
    /*background-color: red;*/
    background-position: center;
    background-size: 150%;
    background-repeat: no-repeat;
    /*background-attachment: scroll;*/
    margin: 5px;
    align-content: center;
    text-align: center;
    transition: 0.5s;
  }
  .pic:hover{
    background-size: 155%;
    transition: 0.5s;
  }
  .teacher-title {
    color: #e4b22b;
    font-size: 24px;
    text-align: center;
    cursor: default;
  }
  .teacher-info {
    color: #FFFFFF;
    font-size: 18px;
    width: 200px;
    text-align: center;
    cursor: default;
  }
  .information {
    transition:all 0.5s;
  }




</style>
