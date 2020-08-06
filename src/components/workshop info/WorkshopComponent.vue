<template>
  <div>
    <div class="header" :style="{backgroundImage: `url(${currentWorkshop.imageURL})`}">
      <h1>{{ currentWorkshop.title }}</h1>
    </div>
    <div class="info row">
      <div class="col-sm-8 bg-info">

      </div>
      <div class="col-sm-4 " style="padding: 10px">
        <div class="presenters">
          <h2 v-if="currentWorkshop.teacher.length === 1">ارائه دهنده</h2>
          <h2 v-if="currentWorkshop.teacher.length !== 1"> ارائه دهنده ها</h2>
        </div>
        <div class="row d-flex justify-content-between">
          <button class="btn changeTeacher" @click="teacherIndexDecrement"><</button>
          <transition name="slide" mode="out-in">
            <app-teacher-info
              :teachers="currentWorkshop.teacher"
              :index="teacherIndex">

            </app-teacher-info>
          </transition>
          <button class="btn changeTeacher" @click="teacherIndexIncrement">></button>
        </div>
      </div>
    </div>
    <button class="btn btn-dark" @click="setCurrentWorkshop(8)">k</button>
  </div>
</template>

<script>
  import TeacherInfo from "./TeacherInfo.vue"

  export default {
    components:{
      appTeacherInfo: TeacherInfo,
    },
    props: ['data'],
    data() {
      return {
        teacherIndex: 0,
        currentWorkshop: {
          title: '',
          teacher: [],
          imageURL: '',
        },
      }
    },
    methods: {
      setCurrentWorkshop(index) {
        this.currentWorkshop = this.data[index];
      },
      teacherIndexIncrement(){
        if (this.teacherIndex !== this.currentWorkshop.teacher.length-1)
          this.teacherIndex++;
      },
      teacherIndexDecrement(){
        if (this.teacherIndex !== 0)
          this.teacherIndex--;
      },
    }
  }
</script>

<style scoped>
  .header {
    /*background-color: red;*/
    background-size: 100%;
    /*background-attachment: fixed;*/
    /*filter: brightness(0.8) ;*/
    background-position: center;
    width: 100%;
    height: 200px;
    text-align: center;
    transition: all 0.5s;
    font-size: 35px;
    box-shadow: 0 0 50px 0 black inset;
    /*position: relative;*/
  }
  .header:hover{
    font-size: 40px;
    background-size: 105%;
  }

  .header h1 {
    /*position: absolute;*/
    cursor: default;
    color: #FFFFFF;
    text-shadow: 0 0 20px black;
    font-weight: bolder;
    padding-top: 90px;
  }

  .info {
    background-color: #292929;
    margin: 50px;
    border-radius: 30px;

    height: 500px;
  }
  .presenters{
    cursor: default;
    color: #e4b22b;
    text-align: center;
    font-weight: bolder;

  }
  .presenters h2{
    font-size: 28px;
    padding: 10px;
  }
  .changeTeacher {
    color: #FFFFFF;
  }
  .changeTeacher:hover {
    color: #e4b22b;
  }








  .slide-enter{
    opacity: 0;
  }
  .slide-enter-active{
    animation: slide-in 1s ease-out forwards;
    opacity: 1;
    transition: opacity 1s;
  }
  .slide-leave{
    opacity: 1;
  }
  .slide-leave-active{
    animation: slide-out 1s ease-out forwards;
    opacity: 0;
    transition: opacity 1s;
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
      transform: translateX(0);
    }
    to{
      transform: translateX(+20px);
    }
  }
</style>
