<script setup lang="ts">
import { ref } from "vue";

const locations = ["새롬관", "서초"];
const locationName = ref("새롬관");
const locationClicked = ref(false);
const locationOptionHandler = (index: number) => {
  locationName.value = locations[index];
  locationClicked.value = false;
};
</script>

<template>
  <nav class="nav">
    <div class="logo">
      <div><img src="@/assets/images/logo.svg" alt="" /></div>
      <div class="locationSelectBox">
        <span @click="locationClicked = !locationClicked">{{
          locationName
        }}</span>
        <ul v-if="locationClicked" class="optionList">
          <li
            v-for="(location, i) in locations"
            :key="i"
            @click="locationOptionHandler(i)"
            class="optionItem"
          >
            {{ location }}
          </li>
        </ul>
      </div>
    </div>
    <div class="map"><img src="@/assets/images/map.svg" alt="" /></div>
  </nav>
</template>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--main-color);
  padding: 0 20px;
  color: var(--white-color);
  height: 80px;
}
.logo {
  display: flex;
  flex-direction: row;
  align-items: center;
  cursor: pointer;
}
.locationSelectBox {
  position: relative;
  margin-left: 40px;
  font-size: 24px;
  font-family: var(--location-font);
  cursor: pointer;
}

.locationSelectBox > span::after {
  content: "";
  position: absolute;
  right: -20px;
  top: 50%;
  transform: translateY(-50%);
  width: 20px;
  height: 20px;
  background: url(@/assets/images/select.svg) no-repeat 100%;
}

.optionList {
  position: absolute;
  top: 30px;
  left: -15px;
  padding: 5px 10px;
  background: var(--white-color);
  opacity: 0.8;
  border-radius: 4px;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
}
.optionItem {
  width: 80px;
  height: 40px;
  color: var(--main-color);
  background: var(--white-color);
  line-height: 40px;
  text-indent: 5px;
}
.optionItem:hover {
  opacity: 0.9;
}
.map {
  cursor: pointer;
}
</style>
