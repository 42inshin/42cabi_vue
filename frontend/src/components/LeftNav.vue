<script setup lang="ts">
import { ref } from "vue";
</script>

<template>
  <nav class="nav">
    <section class="topSection">
      <ul class="topBtns">
        <li>Home</li>
        <li>2층</li>
        <li>3층</li>
        <li>4층</li>
        <li>5층</li>
      </ul>
    </section>
    <section class="bottomSection">
      <ul class="bottomBtns">
        <li>
          <div class="searchIcon"></div>
          Search
        </li>
        <li>
          <div class="LogIcon"></div>
          Log
        </li>
        <li>
          <div class="LogOutIcon"></div>
          Logout
        </li>
      </ul>
    </section>
  </nav>
</template>

<style scoped>
.nav {
  width: 90px;
  height: 100%;
  border-right: 1px solid var(--line-color);
  color: var(--gray-color);
}
.topSection {
  height: 50%;
  position: relative;
}
.topSection::after {
  content: "";
  position: absolute;
  left: 17px;
  bottom: 0;
  margin: 0 auto;
  width: 56px;
  height: 1px;
  background-color: var(--line-color);
}
.topBtns {
  text-align: center;
  padding: 30px 10px;
}
.topBtns > li {
  width: 100%;
  height: 48px;
  line-height: 48px;
  font-weight: 300;
  margin-bottom: 30px;
  border-radius: 10px;
  cursor: pointer;
}
.topBtns > li:hover {
  color: var(--white);
  background-color: var(--main-color);
}
.bottomSection {
  height: 50%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  text-align: center;
  padding: 30px 10px;
}
.bottomBtns > li {
  width: 100%;
  height: 48px;
  font-weight: 300;
  margin-top: 30px;
  border-radius: 10px;
  cursor: pointer;
}
.bottomBtns > li:hover {
  color: var(--main-color);
}
.bottomBtns > li > div {
  width: 24px;
  height: 24px;
  margin: 0 auto;
  margin-bottom: 4px;
}
.bottomBtns > li:hover div {
  filter: invert(33%) sepia(55%) saturate(3554%) hue-rotate(230deg)
    brightness(99%) contrast(107%);
}
.searchIcon {
  background-image: url(src/assets/images/search.svg);
  background-size: cover;
}
.LogIcon {
  background-image: url(src/assets/images/log.svg);
  background-size: cover;
}
.LogOutIcon {
  background-image: url(src/assets/images/close-square.svg);
  background-size: cover;
}
</style>
