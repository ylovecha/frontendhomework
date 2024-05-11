<template>
  <div class="home">
    <div
      class="swiper-container home-swiper swiper-container-initialized swiper-container-vertical"
    >
      <div
        class="swiper-wrapper"
        style="
          transition-duration: 0ms;
          transform: translate3d(0px, -1608px, 0px);
        "
      >
        <div class="swiper-slide" style="height: 804px">
          <div class="home-index fp-page">
            <div class="fp-page__wrap">
              <div class="home-index-logo">
                <img
                  src="data:image/png;base64,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"
                  alt=""
                />
              </div>
              <div class="home-index-slg">
                <!--<img src="/_nuxt/img/slogan@2x.301d3f9.png" alt="" />-->
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
        <div class="swiper-slide swiper-slide-prev" style="height: 804px">
          <div class="home-product fp-page">
            <div class="fp-page__wrap">
              <div
                class="swiper-container home-product-swiper swiper-container-fade swiper-container-initialized swiper-container-horizontal"
              >
                <div class="swiper-wrapper" style="transition-duration: 0ms">
                  <div
                    class="swiper-slide"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(0px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/acec40fce337702c40164a07eb43df61_8967600783993583833.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://fastcdn.mihoyo.com/content-v2/plat/100577/82848bd2282a1cf7c3b3b68f36f1dbf9_196881664372621863.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(-28.3664px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/ff83e8d2ff3bbd4d3458fcce73eb55d9_8896280881150939108.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> Houkai Gakuen 2</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游崩坏系列经典Q版射击游戏。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            末日都市之旅，指尖爽快战斗，开启与少女们的末世物语。
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://www.benghuai.com/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 游戏官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/08/09/2997c3646577c605aa2a3a59afb8b695_5102855849738412851.jpg"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(-1280px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/bf4a984982aa8f8ca961d5298afc0c9f_3817884679908679166.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/663fe95dff54044d7cd5d3a355f61bf7_6089937633900261947.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(-80.2368px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/9b6377159a2ea2c033c406a99bb8e200_1893454564161809799.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> Honkai Impact 3rd</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游崩坏系列3D全视角卡通渲染、次世代动作游戏。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            在被崩坏侵蚀的世界中，勇敢的少女组成的女武神部队，为守护世界而展开了战斗。
                          </p>
                          <p
                            style="white-space: pre-wrap; min-height: 1.5em"
                          ></p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://bh3.mihoyo.com/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 游戏官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/08/09/36c4008a87c245f5c057d7f91c4ee53c_5609068881434679938.png"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(-2560px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/52c8d56d58cf1fd496edb51966c00e43_6361030492463878411.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/8d1f82811b02f86a5c74c329c413f7c4_7122814728754206230.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(0px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/47bc404e6e1f5c84c98a23793de77dcd_3931369823459487780.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> Tears of Themis</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游律政恋爱推理游戏。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            你将扮演新人律师，在与他携手解决离奇委托的过程中，被卷入不为人知的阴谋。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            这是一场恋爱×推理的冒险，你将做出怎样的抉择？
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://wd.mihoyo.com/fab/bdsem"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 游戏官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/08/09/7f4ae3b0b8a8228474c482eb96f85713_7335718778613705158.png"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(-3840px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/e69db0b5b5a9a497be8bd4664e64356c_3542211166492525651.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/58574b8c47e058787cc24049413b7cea_7872872512863208275.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(0px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/e9f77840280f95d106fe10d366347506_3990256051696986081.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> Genshin Impact</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游全新开放世界角色冒险游戏。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            你将在游戏中探索一个被称作「提瓦特」的幻想世界。
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://ys.mihoyo.com/main/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 游戏官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/08/05/397c774ea38a6180eb46a9359effbabc_7047935735519102029.png"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(-5120px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/09/e28651e302fd535b0ad45cf22364a7d4_8626727003449149373.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/09/6c0e9aaa5b9471e32316d11284edb710_2698450106633206665.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(0px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/09/54da4869475fbaea33507df96c9f346f_8560873109620344935.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> Honkai: Star Rail</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p
                            style="
                              white-space: pre-wrap;
                              text-align: right;
                              line-height: 1.9;
                            "
                          >
                            米哈游全新银河冒险策略游戏。
                          </p>
                          <p
                            style="
                              white-space: pre-wrap;
                              text-align: right;
                              line-height: 1.9;
                            "
                          >
                            你将由此探索新的文明，结识新的伙伴，
                          </p>
                          <p
                            style="
                              white-space: pre-wrap;
                              text-align: right;
                              line-height: 1.9;
                            "
                          >
                            在无数光怪陆离的「世界」与「世界」之间展开新的冒险。
                          </p>
                          <p
                            style="
                              white-space: pre-wrap;
                              text-align: right;
                              line-height: 1.9;
                            "
                          >
                            所有你想知道的，都将在群星中找到答案。
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://sr.mihoyo.com/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 游戏官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/10/09/29ef9666d637b65e188addee2d46c1b5_3427221492004810391.jpg"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(-6400px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2022/07/12/eab9793dacd5979301ff04e8ae0ddfc4_6003651578016448784.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2022/07/12/dd6757d0dd9627865f88221bb807178d_701447427251294272.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(0px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2023/01/12/5e465a5f498c41774a328d1a38e3a484_619561523732626502.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> Zenless Zone Zero</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游自研的全新动作游戏。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            在这个空洞灾祸频仍的世界里，崛起了一座另类的城市——「新艾利都」。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            而你将成为串联起空洞与都市的关键少数派，名为「绳匠」的特殊职业人士。
                          </p>
                          <p style="white-space: pre-wrap; text-align: right">
                            这里正等待着见证你的故事。
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://juequling.mihoyo.com/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 游戏官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2022/07/12/70db72d8a5f116e50e01e80b5c3edbae_778250817817036086.jpg"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide swiper-slide-prev"
                    style="
                      width: 1280px;
                      opacity: 0;
                      transform: translate3d(-7680px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/3ad5cf9950de316e5b66480220863b96_2825230367235575806.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/4a30498a7e37d6897c27723e377998df_4453430102298956645.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(0px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/be07bad24d1b938be2b44b0b97b14c10_7983250959525070198.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> MIYOUSHE</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游旗下游戏玩家社区。<br />集合了官方资讯、福利趣闻、实用工具及同人作品。<br />让有爱的小伙伴们相聚在这里，一起聊游戏、找攻略、领奖励。
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://bbs.mihoyo.com/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 产品官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              微信公众号
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/08/09/b850dc9cda4ce5d79bcff34224dfdb11_4680315806624169619.jpg"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="swiper-slide swiper-slide-active"
                    style="
                      width: 1280px;
                      opacity: 1;
                      transform: translate3d(-8960px, 0px, 0px);
                      transition-duration: 0ms;
                    "
                  >
                    <div class="wrapper">
                      <div class="home-product-swiper__banner">
                        <div class="home-product-swiper__banner-board">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/4737b008390624f371027af5e311d4b8_5931925418249586397.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-board-content"
                            style="
                              transform: translate(-1.155px, 0px)
                                scale(1.2, 1.2);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-box">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/c86c8d09f16a90f56ee44a3a19ac92b2_6081395262607720905.png"
                            alt="miHoYo"
                            class="home-product-swiper__banner-game"
                            style="
                              transform: translate(-0.0097px, 0px);
                              backface-visibility: hidden;
                              transform-style: preserve-3d;
                            "
                          />
                        </div>
                        <div class="home-product-swiper__banner-btn">
                          <div class="home-product-swiper__banner-btn-box">
                            <div
                              class="home-product-swiper__banner-btn-box__bg"
                            >
                              <b></b>
                            </div>
                          </div>
                          <div class="home-product-swiper__banner-btn-text">
                            <span>intro video</span>
                          </div>
                        </div>
                      </div>
                      <div class="home-product-swiper__info">
                        <div class="home-product-swiper__info-name">
                          <img
                            src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/e9214d33ca2e19406f1fd511fdf5b9e8_3053264761189050333.png"
                            alt=""
                            class="home-product-swiper__info-name-img"
                          />
                          <span class="enname anim"> N0va Desktop</span>
                        </div>
                        <div class="home-product-swiper__info-slash"></div>
                        <div class="home-product-swiper__info-desc">
                          <p style="white-space: pre-wrap; text-align: right">
                            米哈游旗下动态桌面软件。<br />一键点击唤醒鹿鸣，<br />感受专属陪伴和沉浸式体验。
                          </p>
                        </div>
                        <div class="home-product-swiper__socials">
                          <a
                            href="https://n0va.mihoyo.com/"
                            target="_blank"
                            class="home-product-swiper__social"
                            ><span> 产品官网 </span></a
                          >
                          <div class="home-product-swiper__social">
                            <span>
                              微博
                              <!----></span
                            >
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              抖音
                              <div class="home-product-swiper__social-qrcode">
                                <img
                                  src="https://webstatic.mihoyo.com/upload/static-resource/2021/08/09/e6ff3d1c95fe9d7f67fc7a082459da8c_3447397678047864186.png"
                                  alt="miHoYo"
                                />
                                <b></b></div
                            ></span>
                          </div>
                          <div class="home-product-swiper__social">
                            <span>
                              Bilibili
                              <!----></span
                            >
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
              <div class="home-product-nav">
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/11/320a35c423a3d8ca043d7ee14a8c7925_602536019813937911.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/4080f2eb748823d8c38507c3d7b69b36_936817768851375073.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/03/a103c80cb895bfdfb7496f4233b63158_8329011972047580487.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/09/def1f2abcfc2af0bbe2e5900a60a5ee1_5699547505742166353.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/09/870472d6104dbbe7ea18b27c13763ccb_5300916022261002498.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2022/05/27/3896559583929f643fbe39ec1d6ca1c9_1026345827445617861.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav class="home-product-nav__item">
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/09/c218c585aac4aad0a30ab9a6e0e0794c_3908343860724847173.png"
                    alt="miHoYo"
                  />
                </nav>
                <nav
                  class="home-product-nav__item home-product-nav__item--active"
                >
                  <img
                    src="https://webstatic.mihoyo.com/upload/op-public/2021/10/12/7bca19669fd95c1a961a26dc009c342e_7821980510293425191.png"
                    alt="miHoYo"
                  />
                </nav>
              </div>
            </div>
            <div data-v-5dd2d15e="" class="aside-slogan aside-slogan">
              <img
                data-v-5dd2d15e=""
                src="/_nuxt/img/line.a3e37b6.png"
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
        <div class="swiper-slide swiper-slide-active" style="height: 804px">
          <div class="home-about fp-page">
            <img
              src="@/assets/img/decoration.b195643.png"
              class="home-about-decoration"
            />
            <div data-v-5dd2d15e="" class="aside-slogan aside-slogan">
              <img
                data-v-5dd2d15e=""
                src="@/assets/img/line.a3e37b6.png"
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
                    <div class="home-about-cate-wrap">
                      <div class="span-wrapper">
                        <span> 关于米哈游 </span>
                      </div>
                      <div class="span-wrapper">
                        <span class="tab-dark"> 关于米哈游 </span>
                      </div>
                      <div class="span-wrapper">
                        <span> 关于米哈游 </span>
                      </div>
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
                      <div class="span-wrapper">
                        <span> 发展历程 </span>
                      </div>
                      <div class="span-wrapper">
                        <span class="tab-dark"> 发展历程 </span>
                      </div>
                      <div class="span-wrapper">
                        <span> 发展历程 </span>
                      </div>
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
                      <div class="span-wrapper">
                        <span> 荣誉资质 </span>
                      </div>
                      <div class="span-wrapper">
                        <span class="tab-dark"> 荣誉资质 </span>
                      </div>
                      <div class="span-wrapper">
                        <span> 荣誉资质 </span>
                      </div>
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
        <div class="swiper-slide swiper-slide-next" style="height: 804px">
          <div
            class="home-join fp-page"
            values-res="[object Object]"
            join-res="[object Object]"
          >
            <img
              src="/_nuxt/img/decoration.560b085.png"
              class="home-join-decoration"
            />
            <div class="fp-page__wrap">
              <div class="wrapper">
                <div class="banner">
                  <div data-v-5dd2d15e="" class="aside-slogan aside-slogan">
                    <img
                      data-v-5dd2d15e=""
                      src="/_nuxt/img/line.a3e37b6.png"
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
                  <div class="banner__role">
                    <img
                      src="/_nuxt/img/char1.fd8e575.png"
                      alt=""
                      class="banner__role-role1"
                      style="
                        transform: translate(-5.325px, 0px);
                        backface-visibility: hidden;
                        transform-style: preserve-3d;
                      "
                    />
                    <img
                      src="/_nuxt/img/char2.a865d48.png"
                      alt=""
                      class="banner__role-role2"
                      style="
                        transform: translate(-26.6252px, 0px);
                        backface-visibility: hidden;
                        transform-style: preserve-3d;
                      "
                    />
                    <img
                      src="/_nuxt/img/char3.629df8e.png"
                      alt=""
                      class="banner__role-role3"
                      style="
                        transform: translate(-18.6376px, 0px);
                        backface-visibility: hidden;
                        transform-style: preserve-3d;
                      "
                    />
                  </div>
                  <a href="https://jobs.mihoyo.com/" target="_blank"
                    ><div class="home-join-btn home-join-btn--social">
                      <div class="home-join-btn--blue"></div>
                      <img
                        src="data:image/png;base64,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"
                        class="home-join-btn__arrow"
                      />
                      <div class="home-join-btn__txt">
                        <div class="home-join-btn__title">社会招聘</div>
                        <div class="home-join-btn__subtitle">
                          MORE INFORMATION
                        </div>
                      </div>
                    </div></a
                  >
                  <a href="https://campus.mihoyo.com/" target="_blank"
                    ><div class="home-join-btn home-join-btn--campus">
                      <div class="home-join-btn--blue"></div>
                      <img
                        src="data:image/png;base64,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"
                        class="home-join-btn__arrow"
                      />
                      <div class="home-join-btn__txt">
                        <div class="home-join-btn__title">校园招聘</div>
                        <div class="home-join-btn__subtitle">
                          MORE INFORMATION
                        </div>
                      </div>
                    </div></a
                  >
                </div>
              </div>
              <div class="home-join-container">
                <div
                  class="join-weal home-join-weal join-weal--active"
                  join-res="[object Object]"
                >
                  <div class="join-weal-title">
                    <div class="join-weal-title__main">加入米哈游</div>
                    <div class="join-weal-title__sub">development history</div>
                  </div>
                  <div class="join-weal__container">
                    <div class="join-weal-card hasContent">
                      <div class="join-weal-card__number"></div>
                      <div class="join-weal-card__line"></div>
                      <img
                        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAQCAYAAAB6Hg0eAAAAAXNSR0IArs4c6QAAA4JJREFUSEu1VU1oHGUYft5vNpOqbLuZzabpTrbuzCYUKdgeerE/Ui1BpEihIA314KUN4l9PpReLgh489KCoxYqHgliUHvyh1ZvSYuKhEVowUNNkVsPOuMlmdkNDW9LsfK/MUtOZbyZIC85t3p95n3ne53s+ulavP5YN9HMMaSL6SPqiUsp/GIvde3E8/xQz743mCHTVKhqjRCTVnml3/hBBHI/FGTc50z0y2J+dT5tBYdCptbZByMtgrI8USQkcHjTzX6uN1WorJ3X5CwFb4zn6yDaNN9f4mbNgvBzLEa4siZVntvX331J7OsDCZ6bW2A8S3xKQuV/Ed0SG9pU35n9VG2e85mbBPM5AnGnguG3mT6n1ExPcZWzyLwI0HM0x46JtGgeIKIhvIPLmeP5RMM4AWAUM0AJzsKsyUJhSh3WYJnkZiDNNwGErhemZmeYGrOOxJNN82jZ7X1sTWGetnv8uGG8penBkRn8qTQ+O6w8DdAFgfbWHeZmYn7NKhUsPy3SEmfufcDz/gfTguP4RAJ/FmYbPLHc+LNOpwB5UD/8H06nAwkHhyWOdrwA8qOz+bLloHFHF2gHn+l8BOBQTN/i3tsSBLaVeN6FRzx+9p+loqiVBL6wJbLq28KwAfgBRd6QrkMBLaRZyfbZR1DUxDuBxxUI+sU3jdRUUM2uO2/yOCPvTLCQV2FRtfnuGtFC4UV8LJfSGbRofq0M67HbJSyA8qQw5b20yRtJMN1XHwB8r1LV7S3H9QgLY1F9zdiajjQO0URnynl3Mn0yC4nXobv2YuAmIfm7f8p8fGhpaTvS4C+8z6IQiEZdWtD3lcq4axmPAputLfdReHiOimK4A8blt9hxNWYf48+/meWYcVHJXs7p8ulAoLCVAea1jzPIDxY4WAbHXHui59m98FVij0cgu3RU/AdihaOR7q9hzMFXsNf8MCKOq59FKsMuy+upJppojDP4SgPgvz+sAm5xk/ZGcf0G9LgCM1eXt4Z2l0p2EUbr+OwS8HY/zHEu5p1Lqu5E4gWlGDASC+MVysfcbtZ6YmRyveY6Akfgxx6S4K3ZbVs9iAlSt8QqROB2TAuEmQ9tXKeYmEvXe4g7iINxGNpJjZvlqZaDwqVrf0ZjneY/eRtcTarI70Kul0oZmWlO11toeiLYWF6/WqBSN2bT6G7NzFcqIXCzX1pYHNxu/p9WHsX8AMeuatn/+gNgAAAAASUVORK5CYII="
                        alt=""
                        class="more-btn"
                      />
                      <div class="join-weal-card__brief">
                        <div class="join-weal-card__title">技术宅拯救世界</div>
                        <div class="join-weal-card__content">
                          <div class="join-weal-card__info">
                            <div class="join-weal-card__info-subtitle">
                              技术密集型公司
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              精英化团队理念
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              面向未来的产品
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__desc col3">
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            技术密集型公司
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap">
                              行业领先卡通渲染、人工智能、云游戏技术
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              不断探索前沿科技，是一件很酷的事情
                            </p>
                          </div>
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            精英化团队理念
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap">高人才密度</p>
                            <p style="white-space: pre-wrap; text-align: left">
                              全球化团队
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              与优秀的人在一起，做卓越的事情，获得最好的回报
                            </p>
                          </div>
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            面向未来的产品
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap">始终敢为人先</p>
                            <p style="white-space: pre-wrap; text-align: left">
                              致力于为用户提供美好的、超出想象的产品与体验
                            </p>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__slide">
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--pre"
                        ></span>
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--next"
                        ></span>
                      </div>
                    </div>
                    <div class="join-weal-card">
                      <div class="join-weal-card__number"></div>
                      <div class="join-weal-card__line"></div>
                      <img
                        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAQCAYAAAB6Hg0eAAAAAXNSR0IArs4c6QAAA4JJREFUSEu1VU1oHGUYft5vNpOqbLuZzabpTrbuzCYUKdgeerE/Ui1BpEihIA314KUN4l9PpReLgh489KCoxYqHgliUHvyh1ZvSYuKhEVowUNNkVsPOuMlmdkNDW9LsfK/MUtOZbyZIC85t3p95n3ne53s+ulavP5YN9HMMaSL6SPqiUsp/GIvde3E8/xQz743mCHTVKhqjRCTVnml3/hBBHI/FGTc50z0y2J+dT5tBYdCptbZByMtgrI8USQkcHjTzX6uN1WorJ3X5CwFb4zn6yDaNN9f4mbNgvBzLEa4siZVntvX331J7OsDCZ6bW2A8S3xKQuV/Ed0SG9pU35n9VG2e85mbBPM5AnGnguG3mT6n1ExPcZWzyLwI0HM0x46JtGgeIKIhvIPLmeP5RMM4AWAUM0AJzsKsyUJhSh3WYJnkZiDNNwGErhemZmeYGrOOxJNN82jZ7X1sTWGetnv8uGG8penBkRn8qTQ+O6w8DdAFgfbWHeZmYn7NKhUsPy3SEmfufcDz/gfTguP4RAJ/FmYbPLHc+LNOpwB5UD/8H06nAwkHhyWOdrwA8qOz+bLloHFHF2gHn+l8BOBQTN/i3tsSBLaVeN6FRzx+9p+loqiVBL6wJbLq28KwAfgBRd6QrkMBLaRZyfbZR1DUxDuBxxUI+sU3jdRUUM2uO2/yOCPvTLCQV2FRtfnuGtFC4UV8LJfSGbRofq0M67HbJSyA8qQw5b20yRtJMN1XHwB8r1LV7S3H9QgLY1F9zdiajjQO0URnynl3Mn0yC4nXobv2YuAmIfm7f8p8fGhpaTvS4C+8z6IQiEZdWtD3lcq4axmPAputLfdReHiOimK4A8blt9hxNWYf48+/meWYcVHJXs7p8ulAoLCVAea1jzPIDxY4WAbHXHui59m98FVij0cgu3RU/AdihaOR7q9hzMFXsNf8MCKOq59FKsMuy+upJppojDP4SgPgvz+sAm5xk/ZGcf0G9LgCM1eXt4Z2l0p2EUbr+OwS8HY/zHEu5p1Lqu5E4gWlGDASC+MVysfcbtZ6YmRyveY6Akfgxx6S4K3ZbVs9iAlSt8QqROB2TAuEmQ9tXKeYmEvXe4g7iINxGNpJjZvlqZaDwqVrf0ZjneY/eRtcTarI70Kul0oZmWlO11toeiLYWF6/WqBSN2bT6G7NzFcqIXCzX1pYHNxu/p9WHsX8AMeuatn/+gNgAAAAASUVORK5CYII="
                        alt=""
                        class="more-btn"
                        style="display: none"
                      />
                      <div class="join-weal-card__brief">
                        <div class="join-weal-card__title">价值观</div>
                        <div class="join-weal-card__content">
                          <div class="join-weal-card__info">
                            <div class="join-weal-card__info-subtitle">
                              说到做到
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              有话直说
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              只认功劳
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              追求极致
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__desc col4">
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            说到做到
                          </div>
                          <!---->
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            有话直说
                          </div>
                          <!---->
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            只认功劳
                          </div>
                          <!---->
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            追求极致
                          </div>
                          <!---->
                        </div>
                      </div>
                      <div class="join-weal-card__slide">
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--pre"
                        ></span>
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--next"
                        ></span>
                      </div>
                    </div>
                    <div class="join-weal-card hasContent">
                      <div class="join-weal-card__number"></div>
                      <div class="join-weal-card__line"></div>
                      <img
                        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAQCAYAAAB6Hg0eAAAAAXNSR0IArs4c6QAAA4JJREFUSEu1VU1oHGUYft5vNpOqbLuZzabpTrbuzCYUKdgeerE/Ui1BpEihIA314KUN4l9PpReLgh489KCoxYqHgliUHvyh1ZvSYuKhEVowUNNkVsPOuMlmdkNDW9LsfK/MUtOZbyZIC85t3p95n3ne53s+ulavP5YN9HMMaSL6SPqiUsp/GIvde3E8/xQz743mCHTVKhqjRCTVnml3/hBBHI/FGTc50z0y2J+dT5tBYdCptbZByMtgrI8USQkcHjTzX6uN1WorJ3X5CwFb4zn6yDaNN9f4mbNgvBzLEa4siZVntvX331J7OsDCZ6bW2A8S3xKQuV/Ed0SG9pU35n9VG2e85mbBPM5AnGnguG3mT6n1ExPcZWzyLwI0HM0x46JtGgeIKIhvIPLmeP5RMM4AWAUM0AJzsKsyUJhSh3WYJnkZiDNNwGErhemZmeYGrOOxJNN82jZ7X1sTWGetnv8uGG8penBkRn8qTQ+O6w8DdAFgfbWHeZmYn7NKhUsPy3SEmfufcDz/gfTguP4RAJ/FmYbPLHc+LNOpwB5UD/8H06nAwkHhyWOdrwA8qOz+bLloHFHF2gHn+l8BOBQTN/i3tsSBLaVeN6FRzx+9p+loqiVBL6wJbLq28KwAfgBRd6QrkMBLaRZyfbZR1DUxDuBxxUI+sU3jdRUUM2uO2/yOCPvTLCQV2FRtfnuGtFC4UV8LJfSGbRofq0M67HbJSyA8qQw5b20yRtJMN1XHwB8r1LV7S3H9QgLY1F9zdiajjQO0URnynl3Mn0yC4nXobv2YuAmIfm7f8p8fGhpaTvS4C+8z6IQiEZdWtD3lcq4axmPAputLfdReHiOimK4A8blt9hxNWYf48+/meWYcVHJXs7p8ulAoLCVAea1jzPIDxY4WAbHXHui59m98FVij0cgu3RU/AdihaOR7q9hzMFXsNf8MCKOq59FKsMuy+upJppojDP4SgPgvz+sAm5xk/ZGcf0G9LgCM1eXt4Z2l0p2EUbr+OwS8HY/zHEu5p1Lqu5E4gWlGDASC+MVysfcbtZ6YmRyveY6Akfgxx6S4K3ZbVs9iAlSt8QqROB2TAuEmQ9tXKeYmEvXe4g7iINxGNpJjZvlqZaDwqVrf0ZjneY/eRtcTarI70Kul0oZmWlO11toeiLYWF6/WqBSN2bT6G7NzFcqIXCzX1pYHNxu/p9WHsX8AMeuatn/+gNgAAAAASUVORK5CYII="
                        alt=""
                        class="more-btn"
                      />
                      <div class="join-weal-card__brief">
                        <div class="join-weal-card__title">
                          快乐工作用心成长
                        </div>
                        <div class="join-weal-card__content">
                          <div class="join-weal-card__info">
                            <div class="join-weal-card__info-subtitle">
                              体系化培训助力成长
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              简单纯粹的工作氛围
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__desc col2">
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            体系化培训助力成长
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap">
                              社招新人培训、校招新人培训
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              【阿蒙森计划】Leader培训
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              系列通用&amp;专业课程/沙龙
                            </p>
                          </div>
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            简单纯粹的工作氛围
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap">
                              扁平架构、决策高效
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              问题驱动、务实专注
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              让你在追求极致的路上更加轻松愉快
                            </p>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__slide">
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--pre"
                        ></span>
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--next"
                        ></span>
                      </div>
                    </div>
                    <div class="join-weal-card hasContent">
                      <div class="join-weal-card__number"></div>
                      <div class="join-weal-card__line"></div>
                      <img
                        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAQCAYAAAB6Hg0eAAAAAXNSR0IArs4c6QAAA4JJREFUSEu1VU1oHGUYft5vNpOqbLuZzabpTrbuzCYUKdgeerE/Ui1BpEihIA314KUN4l9PpReLgh489KCoxYqHgliUHvyh1ZvSYuKhEVowUNNkVsPOuMlmdkNDW9LsfK/MUtOZbyZIC85t3p95n3ne53s+ulavP5YN9HMMaSL6SPqiUsp/GIvde3E8/xQz743mCHTVKhqjRCTVnml3/hBBHI/FGTc50z0y2J+dT5tBYdCptbZByMtgrI8USQkcHjTzX6uN1WorJ3X5CwFb4zn6yDaNN9f4mbNgvBzLEa4siZVntvX331J7OsDCZ6bW2A8S3xKQuV/Ed0SG9pU35n9VG2e85mbBPM5AnGnguG3mT6n1ExPcZWzyLwI0HM0x46JtGgeIKIhvIPLmeP5RMM4AWAUM0AJzsKsyUJhSh3WYJnkZiDNNwGErhemZmeYGrOOxJNN82jZ7X1sTWGetnv8uGG8penBkRn8qTQ+O6w8DdAFgfbWHeZmYn7NKhUsPy3SEmfufcDz/gfTguP4RAJ/FmYbPLHc+LNOpwB5UD/8H06nAwkHhyWOdrwA8qOz+bLloHFHF2gHn+l8BOBQTN/i3tsSBLaVeN6FRzx+9p+loqiVBL6wJbLq28KwAfgBRd6QrkMBLaRZyfbZR1DUxDuBxxUI+sU3jdRUUM2uO2/yOCPvTLCQV2FRtfnuGtFC4UV8LJfSGbRofq0M67HbJSyA8qQw5b20yRtJMN1XHwB8r1LV7S3H9QgLY1F9zdiajjQO0URnynl3Mn0yC4nXobv2YuAmIfm7f8p8fGhpaTvS4C+8z6IQiEZdWtD3lcq4axmPAputLfdReHiOimK4A8blt9hxNWYf48+/meWYcVHJXs7p8ulAoLCVAea1jzPIDxY4WAbHXHui59m98FVij0cgu3RU/AdihaOR7q9hzMFXsNf8MCKOq59FKsMuy+upJppojDP4SgPgvz+sAm5xk/ZGcf0G9LgCM1eXt4Z2l0p2EUbr+OwS8HY/zHEu5p1Lqu5E4gWlGDASC+MVysfcbtZ6YmRyveY6Akfgxx6S4K3ZbVs9iAlSt8QqROB2TAuEmQ9tXKeYmEvXe4g7iINxGNpJjZvlqZaDwqVrf0ZjneY/eRtcTarI70Kul0oZmWlO11toeiLYWF6/WqBSN2bT6G7NzFcqIXCzX1pYHNxu/p9WHsX8AMeuatn/+gNgAAAAASUVORK5CYII="
                        alt=""
                        class="more-btn"
                      />
                      <div class="join-weal-card__brief">
                        <div class="join-weal-card__title">优秀的薪酬福利</div>
                        <div class="join-weal-card__content">
                          <div class="join-weal-card__info">
                            <div class="join-weal-card__info-subtitle">
                              诚意满满薪金回报
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              丰富年节福利
                            </div>
                            <div class="join-weal-card__info-subtitle">
                              贴心关爱员工健康
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__desc col3">
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            诚意满满薪金回报
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap; text-align: left">
                              行业领先的薪酬
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              每年两次的薪酬回顾机会
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              优秀的你值得有竞争力的回报
                            </p>
                          </div>
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            丰富年节福利
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap; text-align: left">
                              年会豪礼、多样周边、
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              节日礼品
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              免费晚餐、零食与下午茶
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              360度关爱你的生活
                            </p>
                          </div>
                        </div>
                        <div>
                          <div
                            class="join-weal-card__desc-subtitle"
                            style="font-size: 0.18rem"
                          >
                            贴心关爱员工健康
                          </div>
                          <div class="join-weal-card__desc-content">
                            <p style="white-space: pre-wrap; text-align: left">
                              六险二金、家庭体检
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              EAP心理咨询、
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              10天起步的年假
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              工作与生活平衡，
                            </p>
                            <p style="white-space: pre-wrap; text-align: left">
                              让你在前进路上后顾无忧
                            </p>
                          </div>
                        </div>
                      </div>
                      <div class="join-weal-card__slide">
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--pre"
                        ></span>
                        <span
                          class="join-weal-card__slide-item join-weal-card__slide-item--next"
                        ></span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="swiper-slide" style="height: 804px">
          <div
            class="swiper-container last-swiper swiper-container-initialized swiper-container-vertical swiper-container-free-mode"
          >
            <div
              class="swiper-wrapper"
              style="transform: translate3d(0px, -1px, 0px)"
            >
              <div class="swiper-slide swiper-slide-active">
                <div data-v-f2eaee8a="" class="home-news">
                  <img
                    data-v-f2eaee8a=""
                    src="/_nuxt/img/decoration.7a97c88.png"
                    class="home-news-decoration"
                  />
                  <div
                    data-v-5dd2d15e=""
                    data-v-f2eaee8a=""
                    class="aside-slogan aside-slogan"
                  >
                    <img
                      data-v-5dd2d15e=""
                      src="/_nuxt/img/line.a3e37b6.png"
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
                  <div data-v-f2eaee8a="" class="home-news__wrap">
                    <div data-v-f2eaee8a="" class="home-news-center">
                      <div data-v-f2eaee8a="" class="home-news__content">
                        <a
                          data-v-f2eaee8a=""
                          href="/news/105515"
                          class="home-news-first"
                          ><div
                            data-v-f2eaee8a=""
                            class="home-news-first__info"
                          >
                            <div
                              data-v-f2eaee8a=""
                              class="home-news-first__info-date"
                            >
                              <div data-v-f2eaee8a="">
                                12<span data-v-f2eaee8a="" class="slash">/</span
                                >28
                              </div>
                              <div data-v-f2eaee8a="" class="year">2022</div>
                            </div>
                            <div data-v-f2eaee8a="" class="home-news-first-box">
                              <div
                                data-v-f2eaee8a=""
                                class="home-news-first__title"
                              >
                                <div
                                  data-v-f2eaee8a=""
                                  class="home-news-first__title-content"
                                >
                                  米哈游荣获“全国文化企业30强”
                                </div>
                              </div>
                              <div
                                data-v-f2eaee8a=""
                                class="home-news-first__desc"
                              >
                                12月28日，光明日报社和经济日报社向社会联合发布了第十四届“全国文化企业30强”名单，上海米哈游网络科技股份有限公司等30家企业进入行列。
                              </div>
                            </div>
                            <!---->
                            <div data-v-f2eaee8a="" class="more-icon">
                              <b data-v-f2eaee8a="">read more</b>
                              <img
                                data-v-f2eaee8a=""
                                src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAUCAYAAADLP76nAAAAAXNSR0IArs4c6QAAAkhJREFUWEell0FrE1EUhc+dhBIlgl2ajKAWIlSEomkiSMFKFoLgzj/gotWi0C5sp7usnBhBVKjQuPAfCIKgOy2KZlKDO7ciZlKxIF0UmmbiPHkjFNt5mTfJneWE83G+N3NvEiosuU+IcAeKiwTN1O9nnqk++/8el8HJE66LROGU+5KIrh4sKgR2SYhLTtWsR0pwGYw8yWLj5V/p9I73nggTiqKu/6ebX39w8meUBJcxbD4QkFdxsWXCIHnSWUXRD73fG5ebtbwXJcFlDJPfE5DFLtx1z4kErQEiHSpKWHHs7G3dPHAZg+b3CQQSy+414eMFCIlQWR83nGr2uVaCyRikQ0hAlitYrQUCPVQU7QifphrVzGedBJcRN68UCCSWWk+J6FZoMwE/PDLOf7GPbWolmIw4HfoKBOt1rP2KgCthCbF2OJUtvStTT7teOYwYHfoLALi4uHmkZ3TlZhoPFxWPnYo5r3sKXIYuHylQWG7lSASrdTT0FIhWG3bmpk6Ay9Dl+wqctb6PHkKyTkBOMQcft1Nb01/LZ7pRAlxGnLxaoPw2WezkXgMoKQq2ex0v33x0YiPy9LmMmHmlQNFyVwDMKU5+FySmG7b5SffqcBlx8yGBScudMwApEP4yJpqp2/pfp1zGIPl9ApOWWzIA+eokD7b3IWrrFXNWd/JcxqD5PYHIaQdiDS2XMUw+EJiY/3Z0JDUiN85p5dAaXr55L3pouYxh88EfmuJY+41q4wgg3tByGYw89Zv2f0/Cn3Uqx2u6957L4OT/AhHc47y6QZ8OAAAAAElFTkSuQmCC"
                                alt=""
                              />
                            </div>
                          </div>
                          <div
                            data-v-f2eaee8a=""
                            class="home-news-first__banner"
                          >
                            <div
                              data-v-f2eaee8a=""
                              class="home-news-first__banner-bg"
                            >
                              <div data-v-f2eaee8a="" class="mask">
                                <img
                                  data-v-f2eaee8a=""
                                  src="data:image/png;base64,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"
                                  alt=""
                                  class="text1"
                                />
                                <img
                                  data-v-f2eaee8a=""
                                  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAAAdCAYAAABcz8ldAAAAAXNSR0IArs4c6QAAA8FJREFUaEPlmk/IVVUUxX9LraRITCqowIJKKswyLAwMA4OKgoqCEglKIkiIIKMGCgUlFGREkCJBQgQJDUIciEF/oAYF/S9HTmyggwYNgiD6t2LD+eS+9/k93z7ng+7FM3mTvfa6Z61z7ztn7yPmcdh+ENjXmHKfpI01OWxvAt6twRbM/86thocfgdq+GPgRWNaQ8xiwStKv2Ry2Lwe+AZZksSW+F9zzachB4I5KMQJm4E5Jh7I5bJ8BfA7clMWW+N5wz4shtp8AdlWKMQPbLWlLTQ7bLwPP1WALpjfczYbYvhL4FjinQZAjwGpJv2dz2N4AfAgsyGJLfK+4mwyxvRD4DLi5UoyA/Q3cIumLbA7b5wPfA/H/VTN6x91qyDbgpRolOpgdkrbX5LB9ALi7BlswveOuNsT2aiBW9ZkNgsSuaK2kv7I5bD8JvJHFdeJ7yV1liO2zgK+AlQ2C/AGskXQ4m8P2KuBLYHEWW+J7y11ryKvA1koxZmBbJb2WzWH77LIYrs5iO/G95U4bYns98HHDriZ0+RTYIOnfrKi29wCPZ3Gd+F5zpwyxfS7wA3BZgyC/ldP4z9kctu8H3gdSz93h6T13amK23wYezQo5Fr9Z0t5sDtvLge+A87LYTnzvuac2xPY9wAcNqzN02S/p3qyg5bzzSZxXsthO/CC4pzLE9gXAT8CFDYL8AlwrKX5Tw/bzwAsp0GjwYLinNSTejPTK7mgSxbv7JO3Pimp7HRBvx6IstsQPivuUhth+BEh/88fE2ytpc1ZQ20vL/8alWWwnflDcEw2xHULErqq2xxC6HAWukxQ7nNSwHTuqB1Kg0eDBcc9piO2onn4E3NogSJwz4rwRe//UsP0Y8FYKNBo8SO5JhjwN7GwQJKA7JT2TzWH7qnIabynpD447dDqpIbavAb5uqBVF7qhRRa0q6kZTj1Ini6Ll9VODZgcOjntmCrMMKe3QEOSGBkH+LFXcaFylhu3XgadSoNHgQXJPMuRFoKo/0dFlu6QdWVFt3wVEj+OUu78JuQfH3Z3LyMRtry0dwNo9f+SOt2udpH8yhti+qHT/4hBaOwbHPT7RE4aUsnZ8YlbUqgFETzx649GnnnrYjueIvvhtU4NmBw6O+2Rz7RryJlB166OTeIuk3VlRbT8LvJLFjcUPjntOQ2zfDsS9qpZv9yFJ6XtZtm8sd6paWsGD455r8cl2lLPjxuElDSs0bhpG4fB4Jkfpr0Rv+4oMbix2cNyT5hqGvAc81CBIQDdKSt/ptf0O8PDpxj1pvv8BVQ3mLa1fjFIAAAAASUVORK5CYII="
                                  alt=""
                                  class="text2"
                                />
                              </div>
                              <img
                                data-v-f2eaee8a=""
                                src="https://webstatic.mihoyo.com/upload/op-public/2023/03/10/a0d281d80e74ce5c352d1f165bbe502a_8918873714662926852.png"
                                alt="miHoYo"
                                class="home-news-first__banner-bg-img"
                              />
                            </div>
                            <div
                              data-v-f2eaee8a=""
                              class="home-news-first__banner-img"
                            >
                              <img
                                data-v-f2eaee8a=""
                                src="https://webstatic.mihoyo.com/upload/op-public/2023/03/10/a0d281d80e74ce5c352d1f165bbe502a_8918873714662926852.png"
                                alt="miHoYo"
                              />
                            </div></div
                        ></a>
                        <div data-v-f2eaee8a="" class="home-news-list">
                          <div
                            data-v-f2eaee8a=""
                            class="home-news-list__item home-news-list__item--active"
                          >
                            <span data-v-f2eaee8a=""> 1 </span>
                          </div>
                          <div data-v-f2eaee8a="" class="home-news-list__item">
                            <span data-v-f2eaee8a=""> 2 </span>
                          </div>
                          <div data-v-f2eaee8a="" class="home-news-list__item">
                            <span data-v-f2eaee8a=""> 3 </span>
                          </div>
                        </div>
                      </div>
                      <a data-v-f2eaee8a="" href="/news" class=""
                        ><div data-v-f2eaee8a="" class="more-btn">
                          查看更多新闻
                        </div></a
                      >
                    </div>
                  </div>
                </div>
              </div>
              <div class="swiper-slide swiper-slide-next">
                <footer id="swiper-footer">
                  <div>
                    <div
                      x-ms-format-detection="none"
                      class="mihoyo-cn-footer undefined"
                    >
                      <div class="footer-content">
                        <div class="footer-logo">
                          <div style="display: flex; align-items: center">
                            <img
                              src="https://fastcdn.mihoyo.com/mi18n/plat_cn/m202004281054311/upload/f7dcd7ce5ff481132db0e8e5588ea41c_1058604956605839480.png"
                              alt=""
                              class="logo-bigger"
                            />
                          </div>
                          <div></div>
                        </div>
                        <div class="footer-info">
                          <div class="footer-link">
                            <div class="footer-protocol">
                              <div>
                                <a
                                  href="https://user.mihoyo.com/#/privacyAgreement"
                                  class="protocol"
                                  target="_blank"
                                  >隐私政策</a
                                >|
                                <a
                                  href="https://webstatic.mihoyo.com/upload/static-resource/2021/11/06/2bc5f2f06b88aea5380c4babe396cf16_1085792848868029218.pdf"
                                  rel="nofollow"
                                  class="protocol"
                                  target="_blank"
                                  >自律公约</a
                                >|
                                <a
                                  href="https://www.mihoyo.com/company/jubao"
                                  rel="nofollow"
                                  class="protocol"
                                  target="_blank"
                                  >廉政举报</a
                                >|
                                <a
                                  href="https://www.mihoyo.com/company/contact"
                                  rel="nofollow"
                                  target="_blank"
                                  class="contract-us protocol"
                                  >联系我们</a
                                >|
                                <a
                                  href="https://jobs.mihoyo.com/"
                                  rel="nofollow"
                                  target="_blank"
                                  class="join-us protocol"
                                  >加入我们</a
                                >
                              </div>
                            </div>
                          </div>
                          <div class="footer-advice">
                            <p class="advice-info">
                              健康游戏忠告：抵制不良游戏，拒绝盗版游戏。注意自我保护，谨防受骗上当。适度游戏益脑，沉迷游戏伤身。合理安排时间，享受健康生活。
                            </p>
                            <div class="inline-info">
                              <a
                                href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=沪公网安备31010402001113号"
                                rel="nofollow"
                                class="footer-filing-item"
                                target="_blank"
                              >
                                沪公网安备31010402001113号
                              </a>
                              <span class="split-line"> | </span>
                              <span class="footer-filing-item"
                                >增值电信业务经营许可证：沪B2-20190555</span
                              >
                            </div>
                          </div>
                          <div class="footer-filing">
                            <div class="footer-filing-content">
                              <a
                                href="https://beian.miit.gov.cn/#/Integrated/index"
                                rel="nofollow"
                                target="_blank"
                                class="footer-filing-item"
                                >沪ICP备19018275号-4</a
                              ><span class="split-line"> | </span>
                              <span class="footer-filing-item">
                                沪网文〔2022〕1334-052号 </span
                              ><span class="split-line"> | </span>
                            </div>
                            <div class="footer-filing-tip">
                              <span>
                                互联网违法不良信息举报邮箱:
                                tousu@service.mihoyo.com
                              </span>
                              <span>
                                互联网违法不良信息举报电话: 021-60371750
                                （工作时间：每天10点 - 20点）
                              </span>
                            </div>
                          </div>
                          <div class="footer-tip">
                            亲爱的市民朋友，上海警方反诈劝阻电话“962110”系专门针对避免您财产被骗受损而设，请您一旦收到来电，立即接听
                          </div>
                          <!--         <div class="mihoyo-copyright">米哈游公司 版权所有</div>       -->
                          <!--                   <div class="mihoyo-copyright">©2012-2020 米哈游公司 版权所有 </div>       -->
                          <div class="guanai-phone">
                            未成年成长关爱热线：021-60371740
                            （服务时间：8:00-23:00）
                          </div>
                          <div class="mihoyo-copyright">
                            ©miHoYo | 上海米哈游影铁科技有限公司
                          </div>
                          <div class="complaint-phone">
                            客服电话：400-666-6312
                          </div>
                          <div class="footer-icon">
                            <a
                              href="https://v.yunaq.com/certificate?domain=www.mihoyo.com&amp;from=label&amp;code=90020"
                              rel="nofollow"
                              target="_blank"
                              style="
                                background-image: url('https://uploadstatic.mihoyo.com/bh3/upload/officialsites/201911/shiming_1575020038_4113.png');
                              "
                            >
                            </a>
                            <a
                              href="http://www.shjbzx.cn/"
                              rel="nofollow"
                              target="_blank"
                              style="
                                background-image: url('https://uploadstatic.mihoyo.com/bh3/upload/officialsites/201911/jubao_1575020039_5071.png');
                              "
                            >
                            </a>
                            <a
                              href="https://www.12377.cn/"
                              rel="nofollow"
                              target="_blank"
                              style="
                                background-image: url('https://uploadstatic.mihoyo.com/bh3/upload/officialsites/202005/youhai_1589857356_1416.png');
                              "
                            >
                            </a>
                            <a
                              href="http://sq.ccm.gov.cn:80/ccnt/sczr/service/business/emark/toDetail/8955A9DDE1FF8B6CE053010A14ACA87F"
                              rel="nofollow"
                              target="_blank"
                              style="
                                background-image: url('https://uploadstatic.mihoyo.com/bh3/upload/officialsites/201911/culture_1575020039_5478.png');
                              "
                            >
                            </a>
                            <a
                              href="javascript:void(0)"
                              rel="nofollow"
                              style="
                                background-image: url('https://uploadstatic.mihoyo.com/bh3/upload/officialsites/201911/e110_1575020039_7486.png');
                              "
                            >
                            </a>
                            <a
                              href="http://wap.scjgj.sh.gov.cn/businessCheck/verifKey.do?showType=extShow&amp;serial=9031000020190314100540000004452331-SAIC_SHOW_310000-20200120150237277642&amp;signData=MEYCIQCjn9IhIKfUHjPlx9W6xrYPZ4GA73Blopwp0iEzSX0OHQIhAOZm3tnlWLrgVXMtvgp5OibauIgiAa+2d+MQ7qzMIm6t"
                              rel="nofollow"
                              target="_blank"
                              style="
                                background-image: url('https://uploadstatic.mihoyo.com/bh3/upload/officialsites/201911/zhizhao_1575020039_4362.png');
                              "
                            >
                            </a>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </footer>
              </div>
            </div>
            <span
              class="swiper-notification"
              aria-live="assertive"
              aria-atomic="true"
            ></span>
          </div>
        </div>
      </div>
      <span
        class="swiper-notification"
        aria-live="assertive"
        aria-atomic="true"
      ></span>
    </div>
    <div
      data-v-162f564a=""
      class="scroll-btn aside-scroll scroll-btn--dark"
      style=""
    >
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
