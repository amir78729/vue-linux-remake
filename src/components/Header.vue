<template>
  <div class="">
    <nav class="navbar header">
      <div class="collapse navbar-collapse d-flex header container-fluid" id="navbarSupportedContent">
        <div class="row col-md-8">
          <button class="btn header-register-btn">ثبت نام کارگاه‌ها</button>
          <div class="header-divider"></div>
          <button class="btn header-regular-btn">ورود به حساب کاربری</button>
        </div>
        <div class="col-md-4 row">
          <button class="btn header-regular-btn">کارگاه‌ها و سخنرانی‌ها</button>
          <div class="header-divider"></div>
          <button class="btn header-regular-btn">درباره جشنواره</button>
          <div class="header-divider"></div>
          <button class="btn header-regular-btn">خانه</button>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style>
  .header {
    background-color: #521C39;
  }
  .header-divider {
    border-left: 2px solid #e4b22b;
    width: 1px;
    margin: 0 3px 0 3px;
  }
  .header-register-btn {
    color: white;
    margin-right: 15px;
    background-color: #e4b22b;
    font-size: 14px;
    height: 40px;
    transition: all 0.3s;

  }
  .header-register-btn:hover {
    background-color: white;
    color: #521C39;
    border-radius: 20px;
    transition: all 0.3s;
  }
  .header-regular-btn {
    color: white;
    font-size: 14px;
  }
  .header-regular-btn:hover{
    color: #e4b22b;
    font-size: 14px;
  }
</style>
