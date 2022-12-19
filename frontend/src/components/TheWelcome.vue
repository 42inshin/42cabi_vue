<script setup lang="ts">
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div id="loginPage" class="wrapper">
    <section class="leftLoginPage">
      <div class="topContents">
        <p>42서울 캐비닛 서비스</p>
        <p class="lightPuple">여러분의 일상을 가볍게</p>
      </div>
      <div class="loginImg">
        <img src="@/assets/images/loginImg.svg" alt="" />
      </div>
      <div class="bottomContents">
        <p><span>Cabi</span>로</p>
        <p>일상의 무게를 덜어보세요.</p>
      </div>
    </section>
    <div class="rightLoginPage">
      <div class="loginCard modal">
        <div class="loginLogo">
          <img src="@/assets/images/logo.svg" alt="" />
        </div>
        <div class="loginTitle">
          <h1>42Cabi</h1>
          <p>여러분의 일상을 가볍게</p>
        </div>
        <button @click="$router.push('/main')">L O G I N</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  width: 100%;
  height: 100%;
}
.leftLoginPage {
  width: 50%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding-left: 7%;
}
.loginImg {
  margin-top: 10%;
  margin-bottom: 10%;
}
.leftLoginPage p {
  font-size: 2rem;
  font-family: var(--main-font);
  font-weight: 700;
  line-height: 3rem;
}
.leftLoginPage p > span {
  color: var(--main-color);
}
.rightLoginPage {
  background-color: var(--main-color);
  width: 50%;
  height: 100%;
}
.lightPuple {
  color: var(--lightpurple-color);
}
.bottomContents p {
  font-size: 1.75rem;
}

/* loginCard */
.rightLoginPage {
  display: flex;
  justify-content: center;
  align-items: center;
}
.loginCard {
  width: 350px;
  height: 500px;
  background-color: var(--white-color);
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  padding: 85px 0;
}
.loginLogo {
  width: 70px;
  height: 70px;
}
.loginTitle {
  text-align: center;
  margin-top: -40px;
}
.loginTitle h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}
.loginTitle p {
  color: var(--main-color);
}
</style>
