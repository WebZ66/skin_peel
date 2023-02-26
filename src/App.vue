<template>
  <div id="app">
    <div class="box">
      <button @click="changeTheme">切换主题</button>
      <button class="btn">不同主题颜色按钮</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    changeTheme() {
      let html = document.querySelector("html");
      if (html.getAttribute("data-theme") == "light") {
        html.setAttribute("data-theme", "dark");
      } else {
        html.setAttribute("data-theme", "light");
      }
    },
  },
};
</script>
<style lang="scss" scoped>
@import "./style/theme.scss";
.box {
  border: 1px solid red;
  width: 100%;
  height: 500px;
}
.btn {
  width: 100px;
  height: 100px;
  border: none;
  @include bg_color("bg_color");
}
</style>