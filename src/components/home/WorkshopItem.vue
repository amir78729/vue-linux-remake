<template>
  <div dir="rtl" class="row item">
    <div class="col-xl-5 col-lg-5 col-md-4 col-sm-5 col-xs-6 bg-dark item-img d-flex" :style="{backgroundImage: `url(${imageURL})`}">
    </div>
    <div class="col-xl-7 col-lg-7 col-md-8 col-sm-7 col-xs-6 item-text" style="position: relative;cursor: default">
      <h4 style="font-weight: bolder; font-size: 20px; text-align: center; margin-bottom: -15px">{{ title }}</h4>
      <hr style="background-color: #e4b22b; margin-bottom: 10px">
      <div>
        <div>
          <div class="row" style="margin-right: 5px">
            <h5 style="font-size: 15px" v-if="teachers.length === 1">مدرس :</h5>
            <h5 style="font-size: 15px" v-else>مدرسین :</h5>
          </div>
          <h5 style="font-size: 18px" v-for="teacher in teachers">{{ teacher.teacherName }}</h5>
        </div>
      </div>
      <div style="position: absolute; bottom: 0; width: calc(100% - 60px); align-content: center ; margin: 30px 0px 30px 30px">
        <button dir="rtl" class="btn button" style="align-content: center" @click="setWorkshop"><span>توضیحات </span></button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        index: -1
      }
    },
    props: ['title', 'imageURL', 'teachers', 'index'],
    methods: {
      setWorkshop(){
        this.$emit('setIndex', this.index)
      }
    }
  }
</script>

<style scoped>
  .item {
    background-color: #292929;
    color: white;
    transition: all 0.3s;
    border-radius: 20px;
    height: 270px;
    margin: 10px 10px 30px 10px;
  }
  .item:hover {
    background-color: #521C39;
    color: #e4b22b;
    box-shadow: 0 0 15px 0 black;
    border-radius: 10px;
  }
  .item:hover .button{
    border-radius: 20px;
  }
  .item:hover .item-img {
    border-radius: 0 10px 10px 0;
    transition: all 0.3s;
    border-left: solid 2px #e4b22b;
  }
  .item-text {
    min-width: 150px;
    padding: 30px;
    text-align: right;
  }
  .item-img {
    /*background: url(${this.imageURL}) no-repeat center / 250%;*/
    border-radius: 0 20px 20px 0;
    transition: all 0.3s;
    border-left: solid 2px white;
    height: inherit;
    background-repeat: no-repeat;
    background-size: 250%;
    /*object-fit: fill;*/
    background-position: center;
    filter: brightness(0.8);
  }
  .item-img:hover {
    filter: brightness(1);
    background-size: 270%;
  }
  .button {
    border-radius: 4px;
    background-color: #e4b22b;
    border: none;
    color: #FFFFFF;
    text-align: center;
    font-size: 14px;
    /*padding: 20px;*/
    width: 100%;
    transition: all 0.5s;
    cursor: pointer;
    height: 40px;
    /*margin: 5px;*/
  }

  .button span {
    cursor: pointer;
    display: inline-block;
    position: relative;
    transition: 0.5s;
  }

  .button span:after {
    content: '...';
    position: absolute;
    opacity: 0;
    top: 0;
    /*right: -20px;*/
    left: -20px;
    transition: 0.5s;
  }

  .button:hover span {
    /*padding-right: 25px;*/
    padding-left: 25px;
  }

  .button:hover span:after {
    opacity: 1;
    /*right: 0;*/
    left: 0;
  }

</style>
