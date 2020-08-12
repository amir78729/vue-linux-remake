<template>
  <div class="snapp">
    <div>
      <transition name="fade-slow" appear>
        <h1>حامی ما</h1>
      </transition>
      <transition name="fade" appear>
        <p data-aos-="zoom-in">
          تیم فنی اسنپ از بدو شروع به کار تاکنون با قدرت گرفتن از ابزارهای متن‌باز (open source) و سیستم عامل لینوکس، اقدام به پیاده‌سازی زیرساختی امن، قابل اطمینان و مقیاس‌پذیر، در اسنپ کرده‌است. در این زیرساخت، تمامی سرورها از سیستم‌عامل لینوکس استفاده کرده و از ابزار‌های مجازی‌سازی مختلفی برای اشتراک منابع، استفاده می‌شود. در کنار این سیستم‌عامل، نرم‌افزارهای متن‌باز، لایه‌های دیگر زیرساخت اسنپ را نیز تشکیل می‌دهند. با رشد تیم فنی اسنپ و افزایش تعداد کاربران، اسنپ با هدف بهبود سرعت عملکرد در توسعه کد و بهینه‌سازی منابع، تصمیم به تشکیل تیم cloud و استفاده از تکنولوژی‌های این حوزه کرد. این تیم با استفاده از فناوری‌هایی مانند “kubernetes” و “openstack” تلاش می‌کند تا مطمئن‌ترین و بهینه‌ترین سرویس را برای کاربران خود، فراهم کند. باتوجه به موارد ذکر شده، اسنپ با استفاده از این زیرساخت، قابلیت خدمت‌رسانی به بیش‌از ۲ میلیون کاربر روزانه را دارد.
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
  .snapp {
    cursor: default;
    text-align: justify;
    direction: rtl;
    padding: 60px;
    color: white;
    background: #521C39 url("https://cdn.discordapp.com/attachments/732234196487241741/740850505898655784/snapp.png") no-repeat center / 100%;
    border-bottom:5px solid rgb(242,169,56);
    transition: all 0.5s ease;
  }
  .snapp:hover {
    background: #521C39 url("https://cdn.discordapp.com/attachments/732234196487241741/740850505898655784/snapp.png") no-repeat center / 105%;
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
