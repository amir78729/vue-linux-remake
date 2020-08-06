<template>
  <div dir="rtl" class="row item">
    <div class="col-xl-5 col-lg-5 col-md-4 col-sm-6 col-xs-6 bg-info item-img">
    </div>
    <div class="col-xl-7 col-lg-7 col-md-8 col-sm-6 col-xs-6 item-text">
      <h4 style="font-weight: bolder; font-size: 20px; text-align: center; margin-bottom: -15px">{{ title }}</h4>
      <hr style="background-color: #e4b22b; margin-bottom: 10px">
      <div class="row">
        <h5 v-if="names.length === 1">مدرس</h5>
        <h5 v-else>مدرسین</h5>
      </div>
      <h5 style="font-size: 18px" v-for="name in names">{{ name }}</h5>
      <button dir="rtl" class="btn button" style="align-content: center"><span>توضیحات بیشتر </span></button>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        // hasOneTeacher: true,
        title: 'عنوان',
        names: ['name1', 'name2', 'name3']
      }
    },
    props: ['title', 'names']
  }
</script>

<style scoped>
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
  .item:hover .button{
    border-radius: 20px;
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
