<script setup>
import home_about_decoration from "@/assets/img/decoration.b195643.png";
import aside_slogan__line from "@/assets/img/line.a3e37b6.png";
</script>
<template>
  <div class="home">
    <div
      class="swiper-container home-swiper swiper-container-initialized swiper-container-vertical"
    >
      <div
        class="swiper-wrapper"
        style="
          transition-duration: 0ms;
          transform: translate3d(0px, -1528px, 0px);
        "
      >
        <div class="swiper-slide" style="height: 764px">
          <div class="home-index fp-page">
            <div class="fp-page__wrap">
              <div class="home-index-logo">
                <img
                  src="data:image/png;base64,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"
                  alt=""
                />
              </div>
              <div class="home-index-action">
                <div class="home-index-btn"><b></b></div>
              </div>
              <div data-v-162f564a="" class="scroll-btn scroll-tip">
                <div data-v-162f564a="" class="scroll-btn__mouse"></div>
                <div data-v-162f564a="" class="scroll-btn__arrow">
                  <img
                    data-v-162f564a=""
                    src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDIxLjAuMCwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSImI3g3QkFEOyYjeDU5MzQ7XyYjeDYyRjc7JiN4OEQxRDtfMV8iDQoJIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4IiB2aWV3Qm94PSIwIDAgOCAxMSINCgkgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgOCAxMTsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGcgaWQ9IiYjeDdCQUQ7JiN4NTkzNDtfJiN4NjJGNzsmI3g4RDFEOyI+DQoJPGc+DQoJCTxwb2x5Z29uIHN0eWxlPSJmaWxsLXJ1bGU6ZXZlbm9kZDtjbGlwLXJ1bGU6ZXZlbm9kZDtmaWxsOiNGRkZGRkY7IiBwb2ludHM9IjUsNy45OTggNSwwIDMuMDAxLDAgMy4wMDEsOCAwLDQuOTk5IDAsNi45OTkgDQoJCQkzLjAwMSwxMCA0LjAzMywxMSA1LDkuOTk4IDgsNi45OTkgOCw0Ljk5OSAJCSIvPg0KCTwvZz4NCjwvZz4NCjwvc3ZnPg0K"
                    alt="miHoYo"
                  />
                </div>
                <div
                  data-v-162f564a=""
                  class="scroll-btn__line"
                  style="display: none"
                ></div>
              </div>
            </div>
            <div class="home-index-bg">
              <video
                src="https://webstatic.mihoyo.com/upload/op-public/2021/08/12/c7f405d6cbb03e5c668a12d3e0de290a_2683598109381103734.mp4"
                poster="https://webstatic.mihoyo.com/upload/op-public/2021/08/12/7a388979f57b0943e38a4fd33ea6d593_3621961254475262927.png"
                autoplay="autoplay"
                autobuffer=""
                x5-video-player-type="h5"
                x-webkit-airplay=""
                playsinline=""
                webkit-playsinline=""
                loop="loop"
                muted="muted"
              ></video>
            </div>
            <!---->
            <div class="home-index-bg__mask"></div>
          </div>
        </div>
        <div class="swiper-slide swiper-slide-prev" style="height: 764px">
          <div class="home-product fp-page">
            <div data-v-5dd2d15e="" class="aside-slogan aside-slogan">
              <img
                data-v-5dd2d15e=""
                :src="aside_slogan__line"
                alt="miHoYo"
                class="aside-slogan__line"
                style="display: none"
              />
              <img
                data-v-5dd2d15e=""
                src="data:image/png;base64,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"
                alt="miHoYo"
                class="aside-slogan__text"
              />
            </div>
            <!---->
          </div>
        </div>
        <!------------------------------------------------------------------------------>
        <div class="swiper-slide swiper-slide-active" style="height: 764px">
          <div class="home-about fp-page">
            <img :src="home_about_decoration" class="home-about-decoration" />
            <div data-v-5dd2d15e="" class="aside-slogan aside-slogan">
              <img
                data-v-5dd2d15e=""
                :src="aside_slogan__line"
                alt="miHoYo"
                class="aside-slogan__line"
              />
              <img
                data-v-5dd2d15e=""
                src="data:image/png;base64,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"
                alt="miHoYo"
                class="aside-slogan__text"
              />
            </div>
            <div class="fp-page__wrap">
              <div class="home-about-cates">
                <div
                  class="home-about-cates-wrap home-about-cates-wrap--active"
                >
                  <div class="home-about-cate">
                    <div
                      class="home-about-cate-wrap"
                      style="
                        transform: translateY(-0.6rem);
                        transition-duration: 0ms;
                      "
                    >
                      <div class="span-wrapper"><span> 关于米哈游 </span></div>
                      <div class="span-wrapper">
                        <span class="tab-dark"> 关于米哈游 </span>
                      </div>
                      <div class="span-wrapper"><span> 关于米哈游 </span></div>
                    </div>
                  </div>
                </div>
                <div class="home-about-cates-wrap">
                  <div class="home-about-cate">
                    <div
                      class="home-about-cate-wrap"
                      style="
                        transform: translateY(-0.6rem);
                        transition-duration: 0ms;
                      "
                    >
                      <div class="span-wrapper"><span> 发展历程 </span></div>
                      <div class="span-wrapper">
                        <span class="tab-dark"> 发展历程 </span>
                      </div>
                      <div class="span-wrapper"><span> 发展历程 </span></div>
                    </div>
                  </div>
                </div>
                <div class="home-about-cates-wrap">
                  <div class="home-about-cate">
                    <div
                      class="home-about-cate-wrap"
                      style="
                        transform: translateY(-0.6rem);
                        transition-duration: 0ms;
                      "
                    >
                      <div class="span-wrapper"><span> 荣誉资质 </span></div>
                      <div class="span-wrapper">
                        <span class="tab-dark"> 荣誉资质 </span>
                      </div>
                      <div class="span-wrapper"><span> 荣誉资质 </span></div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="home-about-container">
                <div class="about-intro">
                  <div class="about-intro__vision">
                    <div class="about-intro__vision-title">
                      我们的愿景
                      <b> Our Vision</b>
                    </div>
                    <div class="about-intro__vision-slg">
                      <div class="anim">
                        <p style="white-space: pre-wrap">
                          2030年，打造出全球十亿人
                        </p>
                        <p style="white-space: pre-wrap; text-align: right">
                          愿意生活在其中的虚拟世界。
                        </p>
                      </div>
                    </div>
                  </div>
                  <div class="about-intro__mihoyo">
                    <div class="about-intro__mihoyo-title">
                      关于米哈游
                      <b> About miHoYo</b>
                    </div>
                    <div class="about-intro__mihoyo-desc">
                      <div>
                        <p style="white-space: pre-wrap">
                          米哈游成立于2011年，致力于为用户提供美好的、超出预期的产品与内容。米哈游陆续推出了多款高品质人气产品，包括《崩坏学园2》、《崩坏3》、《未定事件簿》、《原神》、《崩坏：星穹铁道》，动态桌面软件《人工桌面》以及社区产品《米游社》，并围绕原创IP打造了动画、音乐及周边等多元产品。即将上线的《绝区零》等同样受到全球玩家广泛关注。
                        </p>
                        <p style="white-space: pre-wrap">
                          秉承着“<strong>技术宅拯救世界</strong>”的使命，米哈游始终致力于技术研发、探索前沿科技，在卡通渲染、人工智能、云游戏技术等领域积累了先进的技术能力。
                        </p>
                        <p style="white-space: pre-wrap">
                          米哈游总部位于中国上海，并在新加坡、美国、加拿大、日本、韩国等国家和地区进行全球化布局。目前，公司员工5,000人，来自世界知名游戏/互联网/科技公司。
                        </p>
                        <p style="white-space: pre-wrap; min-height: 1.5em"></p>
                        <p style="white-space: pre-wrap; min-height: 1.5em"></p>
                        <p style="white-space: pre-wrap">
                          <strong>米哈游的研发理念</strong>
                        </p>
                        <p style="white-space: pre-wrap">
                          Something New | Something Exciting | Something Out of
                          Imagination
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <span
        class="swiper-notification"
        aria-live="assertive"
        aria-atomic="true"
      ></span>
    </div>
    <div data-v-162f564a="" class="scroll-btn aside-scroll scroll-btn--dark">
      <div data-v-162f564a="" class="scroll-btn__mouse"></div>
      <div data-v-162f564a="" class="scroll-btn__arrow">
        <img
          data-v-162f564a=""
          src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDIxLjAuMCwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSImI3g3QkFEOyYjeDU5MzQ7XyYjeDYyRjc7JiN4OEQxRDtfMV8iDQoJIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4IiB2aWV3Qm94PSIwIDAgOCAxMSINCgkgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgOCAxMTsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGcgaWQ9IiYjeDdCQUQ7JiN4NTkzNDtfJiN4NjJGNzsmI3g4RDFEOyI+DQoJPGc+DQoJCTxwb2x5Z29uIHN0eWxlPSJmaWxsLXJ1bGU6ZXZlbm9kZDtjbGlwLXJ1bGU6ZXZlbm9kZDtmaWxsOiMzRDQyNEQ7IiBwb2ludHM9IjUsNy45OTggNSwwIDMuMDAxLDAgMy4wMDEsOCAwLDQuOTk5IDAsNi45OTkgDQoJCQkzLjAwMSwxMCA0LjAzMywxMSA1LDkuOTk4IDgsNi45OTkgOCw0Ljk5OSAJCSIvPg0KCTwvZz4NCjwvZz4NCjwvc3ZnPg0K"
          alt="miHoYo"
        />
      </div>
      <div data-v-162f564a="" class="scroll-btn__line"></div>
    </div>
  </div>
</template>
