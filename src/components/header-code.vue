<script>
export default {
  setup() {
    const handleClick = (event) => {
      // 处理点击事件
      event.preventDefault(); // 阻止默认行为，即不跳转到href指定的链接
      // 你的逻辑代码
    };

    return {
      handleClick,
    };
  },
};
//import logoImage from "img/mihoyo-logo.png";
//import { ref } from "vue";
//const logo = ref(logoImage);
</script>
<script setup>
import homeIcon from "@/assets/img/mihoyo-logo.png";
import homeVue from "./home-intro-code.vue";
</script>
<template>
  <div id="__nuxt" style="visibility: visible">
    <div class="container">
      <div class="__vuerscroll">
        <div class="__panel">
          <div class="__view">
            <!--头栏-->
            <div class="header">
              <div class="header__navwrap">
                <div class="header__navbar">
                  <div class="header__navbar-logo">
                    <a href="/index.html" @click="handleClick">
                      <!--logo点击返回主页-->
                      <img :src="homeIcon" />
                    </a>
                  </div>
                  <div class="header__navbar-links">
                    <a href="/" class="header__navbar-link nuxt-link-active"
                      ><span>首页</span><b> 首页</b></a
                    >
                    <div class="header__navbar-link">
                      <span>产品信息</span><b> 产品信息</b>
                    </div>
                    <div
                      class="header__navbar-link header__navbar-link--active"
                    >
                      <span>了解我们</span><b> 了解我们</b>
                    </div>
                    <div class="header__navbar-link">
                      <span>加入我们</span><b> 加入我们</b>
                    </div>
                    <div class="header__navbar-link">
                      <span>新闻动态</span><b> 新闻动态</b>
                    </div>
                    <!---->
                  </div>
                </div>
              </div>
            </div>
            <!----主要内容---->
            <homeVue />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
