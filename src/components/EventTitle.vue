<template>
  <div class="bg">
    <transition name="fade" appear>
      <section dir="rtl" class="row justify-content-center align-content-center">
        <h2 class="title-horizontal">انجمن علمی دانشکده مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر با همکاری اسنپ برگزار می کند:</h2>
        <h1 class="title" >
            <span class="title-yazdahomin">
            یازدهمین دوره
            </span>
          <br>
          <span class="title-jashnvareh">
            جشنواره
            </span>
          <br>
          <span class="title-linux">
            لینوکس
            </span>
          <br>
          <span class="title-amirkabir">
            امیرکبیر
            </span>
        </h1>
      </section>
    </transition>
  </div>
</template>

<style scoped>
  .bg {
    /*background-color: #292929;*/
    width: 100%;
    padding-top:40px;
    padding-bottom:80px;
    min-height:calc(100vh - 64px);
    display: flex;
    align-items:center;
    justify-content:center;
    background: #292929 url("https://cdn.discordapp.com/attachments/732234196487241741/740626481356734847/linus-torvalds.svg") no-repeat center / 70%;
    border-bottom:10px solid rgb(242,169,56);
  }
  .linus {
    /*background-image: url("./src/assets/img/title.png");*/
  }
  .title {
    font-size: 145px;
    font-weight:bolder;
    line-height: 70px;
    color: #e4b22b;
  }
  .title-yazdahomin {
    font-size: 50px;
    word-spacing: -10px;
  }
  .title-jashnvareh {
    font-size: 85px;
  }
  .title-linux {
    font-size: 90px;
  }
  .title-amirkabir {
    font-size: 90px;
  }

  .fade-enter {
    opacity: 0;
  }
  .fade-enter-active {
    transition: opacity 500ms;
  }
  .fade-leave {

  }
  .fade-leave-active {

  }
  .title-horizontal {
    margin-bottom: 60px;
    margin-top: 15px;
    padding-top: 5px;
    padding-bottom: 10px;
    color:white;
    font-size:18px;
    text-align:center;
    writing-mode: vertical-rl;
    text-orientation: mixed;
    height:390px;
    margin-left:10px;
  }
</style>
