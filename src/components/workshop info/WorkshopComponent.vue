<template>
  <div>
    <div class="header" :style="{backgroundImage: `url(${currentWorkshop.imageURL})`}">
      <h1>{{ currentWorkshop.title }}</h1>
    </div>
    <div class="info row">
      <div class="col-sm-8 bg-info">

      </div>
      <div class="col-sm-4 bg-danger">
        <h2 v-if="currentWorkshop.teacher.length === 1">ارائه دهنده</h2>
        <h2 v-if="currentWorkshop.teacher.length !== 1"> ارائه دهنده ها</h2>
        <div class="row d-flex justify-content-between">
          <button @click="teacherIndexDecrement"><</button>
          <app-teacher-info
            :teachers="currentWorkshop.teacher"
            :index="teacherIndex">

          </app-teacher-info>
          <button @click="teacherIndexIncrement">></button>
        </div>
      </div>
    </div>
    <button class="btn btn-dark" @click="setCurrentWorkshop(0)">k</button>
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
        this.teacherIndex++;
      },
      teacherIndexDecrement(){
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
</style>
