<template>
  <div class="info">
    <div>
      <transition name="fade-slow" appear>
        <h1>درباره جشنواره لینوکس امیرکبیر</h1>
      </transition>
      <transition name="fade" appear>
        <p>
          جشنواره‌ی لینوکس امیرکبیر معتبرترین رویداد سالانه‌ و دانشگاهی‌ مرتبط با لینوکس است که هر سال در دانشگاه صنعتی امیرکبیر برگزار می‌شود. این جشنواره شامل کارگاه‌ها و ارائه‌های متعددی در سطوح مبتدی و پیشرفته با موضوعات مرتبط با سیستم عامل متن‌باز لینوکس است. در این جشنواره مجموعه‌ای از ارائه‌ها و کارگاه‌ها ویژه‌ی کاربران مبتدی و حرفه‌ای لینوکس با موضوعاتی مانند مقدمات لینوکس، کرنل، امنیت، برنامه‌نویسی، شبکه، مدیریت سیستم لینوکس و... برگزار می‌شوند.
        </p>
      </transition>
    </div>
  </div>
</template>
<script>

</script>
<style scoped>
  h1 {
    color: #e4b22b;
    font-weight: bolder;
    font-size: 40px;
  }
  .info {
    text-align: justify;
    direction: rtl;
    padding: 60px;
    color: white;
    background: #521C39 url("https://raw.githubusercontent.com/AUT-linux-festival/LinuxFest-Website-Frontend/master/src/assets/img/pinguin.png") no-repeat center / 100%;
    border-bottom:5px solid rgb(242,169,56);
    transition: all 0.5s ease;
  }
  .info:hover {
    /*background: #521C39 url("https://raw.githubusercontent.com/AUT-linux-festival/LinuxFest-Website-Frontend/master/src/assets/img/pinguin.png") no-repeat center / 105%;*/;
    transition: all 0.5s ease;
  }

  .fade-enter {
    opacity: 0;
  }
  .fade-enter-active {
    transition: opacity 1500ms;
    transition-delay: 150ms;
  }
  .fade-leave {

  }
  .fade-leave-active {

  }


  .fade-slow-enter {
    opacity: 0;
  }
  .fade-slow-enter-active {
    animation: slide-in 1s ease-out;
    transition: opacity 1000ms;
  }
  .fade-slow-leave {

  }
  .fade-slow-leave-active {

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
      transform: translateX(0px);
    }
    to{
      transform: translateX(0);
    }
  }
</style>
