<template>
  <div>
    <div class="header" :style="{backgroundImage: `url(${selectedWorkshop.imageURL})`}">
      <h1>{{ selectedWorkshop.title }}</h1>
    </div>
    <div class="info row" >
      <div class="" style="width: 66%; padding: 30px 10px 5px 10px" >
        <h1 style="font-size: 30px; margin-top: 5px" class="presenters">درباره‌ کارگاه</h1>
        <p class="about-workshop" style="cursor: default">{{ selectedWorkshop.info }}</p>
        <hr style="background-color: #e4b22b; width: calc(100% - 100px)">
        <h2 class="sub-header">زمان:</h2>
        <p class="p-info">{{ selectedWorkshop.time }}</p>
        <hr style="background-color: #e4b22b; width: calc(100% - 100px)">
        <h2 class="sub-header">هزینه ثبت نام:</h2>
        <p class="p-info">{{ selectedWorkshop.price }}</p>
        <div>
          <button class="btn reg-btn" >ثبت نام</button>
          <button class="btn reg-btn" @click="goBack">بازگشت</button>
        </div>
      </div>
      <div class="right-panel" style="padding: 10px ; width: 34% ; min-width: 250px">
        <div class="presenters">
          <h2 v-if="selectedWorkshop.teacher.length === 1">ارائه دهنده</h2>
          <h2 v-if="selectedWorkshop.teacher.length !== 1"> ارائه دهنده ها</h2>
        </div>
        <div class="row d-flex justify-content-between">
          <button class="btn changeTeacher" @click="teacherIndexDecrement"><</button>
          <transition name="slide" mode="out-in">
            <app-teacher-info
              :teachers="selectedWorkshop.teacher"
              :index="teacherIndex">
            </app-teacher-info>
          </transition>
          <button class="btn changeTeacher" @click="teacherIndexIncrement">></button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import TeacherInfo from "./TeacherInfo.vue"

  export default {
    components:{
      appTeacherInfo: TeacherInfo,
    },
    props: ['data' , 'workshopIndex', 'selectedWorkshop'],
    data() {
      return {
        teacherIndex: 0,
        currentWorkshop: {
          title: '',
          info: '',
          time:'',
          price:'',
          teacher: [],
          imageURL: '',
        },
      }
    },
    methods: {
      goBack() {
        this.$emit("goBack");
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

  .right-panel{
    border-left: solid #e4b22b 1px;
    background-color: #521C39;
    border-radius: 0px 30px 30px 0px;
  }

  .info {
    background-color: #292929;
    margin: 50px;
    border-radius: 30px;
    min-height: 500px;
  }
  .sub-header{
    color: #e4b22b;
    font-size: 25px;
    direction: rtl;
    text-align: right;
    margin: 0 60px;
    margin-bottom: 10px;
    cursor: default;
  }

  .presenters{
    cursor: default;
    color: #e4b22b;
    text-align: center;
    font-weight: bolder;


  }

  .p-info{
    color: #FFFFFF;
    text-align: right;
    margin: 0 50px;
    cursor: default;

  }
  .about-workshop {
    color: #FFFFFF;
    white-space-treatment: none;
    padding: 0 50px;
    text-align: justify;
  }
  .presenters h2{
    font-size: 28px;
    padding: 10px;
  }
  .changeTeacher {
    color: #FFFFFF;
    outline: none;
  }
  .changeTeacher:hover {
    color: #e4b22b;
  }
  .reg-btn{
    color: #FFFFFF;
    background-color: #e4b22b;
    height: 50px;
    border-radius: 25px;
    width: 200px;
    margin: 40px;
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
