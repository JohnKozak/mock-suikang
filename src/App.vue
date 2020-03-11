<template>
  <div id="app">
    <div class="header">
      <img width="18" height="18" src="@/assets/back.svg" />
      <div class="title">{{title}}</div>
      <div class="title-button-group">
        <img class="btn-group-item" width="16" height="16" src="@/assets/menu.svg" />
        <div class="btn-group-diver"></div>
        <img class="btn-group-item" width="16" height="16" src="@/assets/exit.svg" />
      </div>
    </div>
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data: () => {
    return {
      title: "我的穗康码"
    };
  }
};
</script>

<style>
.header {
  position: fixed;
  /* top: -20px; */
  /* padding-top: 20px; */
  width: -webkit-fill-available;
  padding: 8px;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  justify-content: space-between;
  background-color: rgb(66, 147, 244);
}

.title {
  display: inline-block;
  position: relative;
  left: 32px;
  font-weight: bold;
  color: white;
}

.title-warp {
  /* position: absolute; */
  /* width: 100%; */
  /* display: flex; */
  /* justify-items: center; */
  /* align-items: center; */
  /* margin-left: -10px; */
  /* text-align: center; */
}

.title {
  /* margin: 0, 2px 0, 2px; */
  /* text-align: center; */
}

.btn-group-item {
  margin: 5pt 8pt 5pt 8pt;
}

img .btn-group-item {
  width: 20px;
  height: 20px;
}

.btn-group-diver {
  height: 16px;
  width: 1px;
  /* border: 1px solid #f0f0f0; */
  margin-left: 3px;
  margin-right: 3px;
  background: #f0f0f055;
}

.title-button-group {
  background-color: #2a2a2a3a;
  /* padding: 5px, 0 5px, 0; */
  /* padding: 2px 6px 2px 6px; */
  border-radius: 20pt;
  display: flex;
  flex-direction: row;
  align-items: center;
  flex-wrap: nowrap;
  border: 1px #d0d0d055 solid;
}
</style>
