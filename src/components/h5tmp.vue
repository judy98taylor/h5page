<template>
  <div class="body">

    <transition name="fade">
      <div class="p p1" v-show="curPage==1">
        <div class="loading1">
          <img class="" src="../assets/img/p1loading2.png" alt="">
          <div class="progressBar"></div>
        </div>
        <div class="loading2">
          <img class="circle" src="../assets/img/p1loading1.png" alt="">
          <img class="logo" src="../assets/img/p1logo.png" alt="">
        </div>

        <div class="txt">
          <img src="../assets/img/p1h.png" alt="">
          <div class="dian">
            <div class="dotting"></div>
          </div>
        </div>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p2" v-show="curPage==2">
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <img class="p2h tada" src="../assets/img/p2h.png" alt="">
        <br>
        <br>
        <br>
        <img class="p2h2" src="../assets/img/p2h2.png" alt="">
        <br>
        <img class="go flash" src="../assets/img/p2go.png" alt="" @click="next()">
      </div>
    </transition>

    <transition name="fade">
      <div class="p p3" v-show="curPage==3">
        <br>
        <br>
        <br>
        <br>
        <img src="../assets/img/p3q.png" alt="" class="suofang">
        <br>
        <img src="../assets/img/p3a1.png" alt="" class="option" @click="addScore($event,15)">
        <img src="../assets/img/p3a2.png" alt="" class="option" @click="addScore($event,20)">
        <img src="../assets/img/p3a3.png" alt="" class="option" @click="addScore($event,10)">
        <img src="../assets/img/p3a4.png" alt="" class="option" @click="addScore($event,5)" style="margin-top: -.2rem;">
        <img class="next" src="../assets/img/p3next.png" alt="" @click="next()" v-show="curScore">
      </div>
    </transition>

    <transition name="fade">
      <div class="p p4" v-show="curPage==4">
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <img src="../assets/img/p4q.png" alt="" class="suofang">
        <br>
        <br>
        <img src="../assets/img/p4a1.png" alt="" class="option" @click="addScore($event,15)">
        <img src="../assets/img/p4a2.png" alt="" class="option" @click="addScore($event,10)" style="margin-top: -.5rem;">
        <img src="../assets/img/p4a3.png" alt="" class="option" @click="addScore($event,5)">
        <img src="../assets/img/p4a4.png" alt="" class="option" @click="addScore($event,20)">
        <img class="next" src="../assets/img/p3next.png" alt="" @click="next()" v-show="curScore">
      </div>
    </transition>

    <transition name="fade">
      <div class="p p5" v-show="curPage==5">
        <br>
        <br>
        <br>
        <br>
        <br>
        <img src="../assets/img/p5q.png" alt="" class="suofang">
        <br>
        <img src="../assets/img/p5a1.png" alt="" class="option" @click="addScore($event,20)">
        <img src="../assets/img/p5a2.png" alt="" class="option" @click="addScore($event,5)">
        <img src="../assets/img/p5a3.png" alt="" class="option" @click="addScore($event,20)">
        <img src="../assets/img/p5a4.png" alt="" class="option" @click="addScore($event,10)">
        <img class="next" src="../assets/img/p3next.png" alt="" @click="next()" v-show="curScore">
      </div>
    </transition>

    <transition name="fade">
      <div class="p p6" v-show="curPage==6">
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <img src="../assets/img/p6q.png" alt="" class="suofang">
        <br>
        <img src="../assets/img/p6a1.png" alt="" class="option" @click="addScore($event,5)">
        <img src="../assets/img/p6a2.png" alt="" class="option" @click="addScore($event,10)">
        <img src="../assets/img/p6a3.png" alt="" class="option" @click="addScore($event,20)" style="margin-top:-.2rem;">
        <img src="../assets/img/p6a4.png" alt="" class="option" @click="addScore($event,15)">
        <img class="next" src="../assets/img/p3next.png" alt="" @click="next()" v-show="curScore">
      </div>
    </transition>

    <transition name="fade">
      <div class="p p7" v-show="curPage==7">
        <br>
        <br>
        <br>
        <br>
        <br>
        <img src="../assets/img/p7q.png" alt="" class="suofang">
        <br>
        <img src="../assets/img/p7a1.png" alt="" class="option" @click="addScore($event,5)">
        <img src="../assets/img/p7a2.png" alt="" class="option" @click="addScore($event,10)">
        <br>
        <img src="../assets/img/p7a3.png" alt="" class="option" @click="addScore($event,20)">
        <br>
        <img src="../assets/img/p7a4.png" alt="" class="option" @click="addScore($event,15)" style="margin-top: -.2rem;">
        <img class="next" src="../assets/img/p3next.png" alt="" @click="next()" v-show="curScore">
      </div>
    </transition>

    <transition name="fade">
      <div class="p p8" v-show="curPage==8">
        <!-- <img src="../assets/img/s100.jpg" alt=""> -->
        <img :src="require('../assets/img/s'+totalScore+'.jpg')" alt="" v-if="curPage==8">
        <a href="https://www.bagevent.com/event/932861?bag_track=ettmpower" class="link" onclick="_hmt.push(['_trackEvent', 'btn', 'click', 'link', 'https://www.bagevent.com/event/932861?bag_track=ettmpower']);">
          <img src="../assets/img/p8link.png" alt="">
          <!-- <p>{{totalScore}}</p> -->
        </a>
      </div>
    </transition>

  </div>
</template>

<script>
  var $ = require("npm-zepto");

  export default {
    name: "h5",
    data() {
      return {
        // curPage: 1,
        curPage: 1,
        curScore: 0,
        totalScore: 0,
        progressValue: 0,
        btnS: 1,
        wxData_share: null,
      };
    },
    // 在实例初始化之后，数据观测 (data observer) 和 event/watcher 事件配置之前被调用。
    beforeCreate: function () {
      // console.log("beforeCreate");
    },
    // 在实例创建完成后被立即调用。在这一步，实例已完成以下的配置：数据观测 (data observer)，属性和方法的运算，watch/event 事件回调。然而，挂载阶段还没开始，$el 属性目前不可见。
    created: function () {
      // console.log("created");
    },
    // 以下钩子在服务器端渲染期间不被调用。
    // 在挂载开始之前被调用：相关的 render 函数首次被调用。
    beforeMount: function () {
      // console.log("beforeMount");
    },
    // el 被新创建的 vm.$el 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，当 mounted 被调用时 vm.$el 也在文档内。
    mounted: function () {
      // console.log("mounted");

      // // 注意 mounted 不会承诺所有的子组件也都一起被挂载。如果你希望等到整个视图都渲染完毕，可以用 vm.$nextTick 替换掉 mounted：
      // this.$nextTick(function() {
      //   // Code that will run only after the
      //   // entire view has been rendered
      // });
      const self = this;
      self.initWxShare();
      // img preload
      function imgPreload(imgList, cbk) {
        let count = 0;
        let progressValue = '';
        imgList.forEach((v, i, a) => {
          let imgObj = new Image();
          imgObj.onload = imgObj.onerror = () => {
            // progress
            progressValue = Math.round(count / imgList.length * 100) + '%';
            if (count === imgList.length - 1) {
              // 隐藏load
              cbk && cbk();
            }
            count++;
          }
          imgObj.src = v;
        });
      }
      let imgList1 = [
        require('../assets/img/p1bg.jpg'),
        require('../assets/img/p2bg.jpg'),
        require('../assets/img/p2h2.png'),
        require('../assets/img/p2h.png'),
        require('../assets/img/p3a4.png'),
        require('../assets/img/p3q.png'),
      ];
      let imgList2 = [
        require('../assets/img/s100.jpg'),
        // require('../assets/img/s90.jpg'),
        // require('../assets/img/s80.jpg'),
        // require('../assets/img/s70.jpg'),
        // require('../assets/img/s60.jpg'),
        // require('../assets/img/s50.jpg'),
        // require('../assets/img/s40.jpg'),
        // require('../assets/img/s30.jpg'),
        // require('../assets/img/s95.jpg'),
        // require('../assets/img/s85.jpg'),
        // require('../assets/img/s75.jpg'),
        // require('../assets/img/s65.jpg'),
        // require('../assets/img/s55.jpg'),
        // require('../assets/img/s45.jpg'),
        // require('../assets/img/s35.jpg'),
        // require('../assets/img/s25.jpg'),
      ];


      imgPreload(imgList1, () => {
        self.curPage = 2;
        imgPreload(imgList2);
      });


      // // location.search
      // let arr = location.search.replace('?', '').split('&');
      // let obj = {};
      // arr.forEach((vv) => {
      //   let k = vv.split('=')[0];
      //   let v = vv.split('=')[1];
      //   obj[k] = v;
      // });
      // // console.log(obj);

      // obj.p && (self.curPage = obj.p);

      // JS判断是否在微信浏览器打开
      try {
        if (browser.versions.mobile) {//判断是否是移动设备打开。browser代码在下面
          var ua = navigator.userAgent.toLowerCase();//获取判断用的对象
          if (ua.match(/MicroMessenger/i) == "micromessenger") {
            //在微信中打开
            console.log('在微信中打开');
          }
          if (ua.match(/WeiBo/i) == "weibo") {
            //在新浪微博客户端打开
            console.log('在新浪微博客户端打开');
          }
          if (ua.match(/QQ/i) == "qq") {
            //在QQ空间打开
            console.log('在QQ空间打开');
          }
          if (browser.versions.ios) {
            //是否在IOS浏览器打开
            console.log('是否在IOS浏览器打开');
          }
          if (browser.versions.android) {
            //是否在安卓浏览器打开
            console.log('是否在安卓浏览器打开');
          }
        } else {
          //否则就是PC浏览器打开
          console.log('否则就是PC浏览器打开');
        }

        var browser = {
          versions: function () {
            var u = navigator.userAgent, app = navigator.appVersion;
            return {         //移动终端浏览器版本信息
              trident: u.indexOf('Trident') > -1, //IE内核
              presto: u.indexOf('Presto') > -1, //opera内核
              webKit: u.indexOf('AppleWebKit') > -1, //苹果、谷歌内核
              gecko: u.indexOf('Gecko') > -1 && u.indexOf('KHTML') == -1, //火狐内核
              mobile: !!u.match(/AppleWebKit.*Mobile.*/), //是否为移动终端
              ios: !!u.match(/\(i[^;]+;( U;)? CPU.+Mac OS X/), //ios终端
              android: u.indexOf('Android') > -1 || u.indexOf('Linux') > -1, //android终端或uc浏览器
              iPhone: u.indexOf('iPhone') > -1, //是否为iPhone或者QQHD浏览器
              iPad: u.indexOf('iPad') > -1, //是否iPad
              webApp: u.indexOf('Safari') == -1 //是否web应该程序，没有头部与底部
            };
          }(),
          language: (navigator.browserLanguage || navigator.language).toLowerCase()
        }

      } catch (error) {
        console.log(error)
      }
    },
    methods: {
      initWxShare() {
        const self = this;
        $.get("/wx/get_wxData_share", {
          url: encodeURIComponent(location.href.split('#')[0])
        }, function (data, status, xhr) {
          console.log(data);
          self.wxData_share = data.data;
          wx.config({
            debug: false, // 开启调试模式,调用的所有api的返回值会在客户端alert出来，若要查看传入的参数，可以在pc端打开，参数信息会通过log打出，仅在pc端时才会打印。
            appId: 'wx43d17d7d013dc48f', // 必填，公众号的唯一标识
            timestamp: self.wxData_share.timestamp, // 必填，生成签名的时间戳
            nonceStr: self.wxData_share.nonceStr, // 必填，生成签名的随机串
            signature: self.wxData_share.signature,// 必填，签名，见附录1
            jsApiList: ['onMenuShareTimeline', 'onMenuShareAppMessage', 'onMenuShareQQ', 'onMenuShareQZone', 'onMenuShareWeibo'] // 必填，需要使用的JS接口列表，所有JS接口列表见附录2
          });

          var share = {
            wx_title: '分享标题',
            wx_content: '分享描述',
            wx_img: 'http://www.ylzbl.com/wx/h5/20171210/wx.jpg',
            wx_link: location.href,
          };
          wx.ready(function () {
            wx.onMenuShareTimeline({
              title: share.wx_title, // 分享标题
              link: share.wx_link, // 分享链接
              imgUrl: share.wx_img, // 分享图标
              success: function () {

              },
              cancel: function () {

              }
            });

            wx.onMenuShareAppMessage({
              title: share.wx_title, // 分享标题
              desc: share.wx_content, // 分享描述
              link: share.wx_link, // 分享链接
              imgUrl: share.wx_img, // 分享图标
              success: function () {

              },
              cancel: function () {
                // 用户取消分享后执行的回调函数
              }
            });
          });

        });
      },
      addScore(e, n) {
        const self = this;
        $('.option').removeClass('on');
        $('.option').addClass('off');
        $(e.target).removeClass('off');
        $(e.target).addClass('on');
        this.curScore = n;
        // console.log('curPage:' + self.curPage + ',curScore:' + self.curScore + ',totalScore:' + self.totalScore);
      },
      next: function () {
        const self = this;
        if (!self.btnS) return;
        self.btnS = 0;

        if (self.curPage == 2) {
          self.curPage++;
        } else if (self.curScore) {
          self.totalScore += self.curScore;
          self.curScore = 0;
          self.curPage++;
        } else {
          console.log('没选，当前页面是第?页:' + self.curPage);
        }
        self.btnS = 1;

        // console.log('curPage:' + self.curPage + ',curScore:' + self.curScore + ',totalScore:' + self.totalScore);

      },
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  *,
  html,
  body {
    margin: 0;
    padding: 0;
    position: relative;
  }

  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    font-weight: normal;
  }

  p {
    font-size: 0.24rem;
    line-height: 1.5;
  }

  ul {
    list-style-type: none;
  }

  img {
    width: 100%;
    display: block;
  }

  img:not([src]) {
    visibility: hidden;
  }

  .df {
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
  }

  /* 无box相关支持 使用inline-block hack */

  .fww {
    flex-wrap: wrap;
  }

  .fdr {
    flex-direction: row;
  }

  .fdc {
    flex-direction: column;
  }

  .jcc {
    justify-content: center;
    box-align: center;
    -webkit-box-align: center;
  }

  .jcfs {
    justify-content: flex-start;
  }

  .jcfe {
    justify-content: flex-end;
  }

  .jcsb {
    justify-content: space-between;
  }

  .jcsa {
    justify-content: space-around;
  }

  .acfs {
    /*align-content: flex-start;*/
    /*align-items: flex-start;*/
    align-self: flex-start;
  }

  .ais {
    align-items: stretch;
  }

  .aic {
    align-items: center;
    box-pack: center;
    -webkit-box-pack: center;
  }

  .f1 {
    -webkit-box-flex: 1;
    -moz-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    position: relative;
  }

  /* 兼容ios8 */

  /* IE 不支持 box-pack 和 box-align 属性。 */

  .jcc.aic {
    box-align: center;
    -webkit-box-align: center;
    box-pack: center;
    -webkit-box-pack: center;
  }

  /*.f1:nth-child(1) {
  background-color: red;
}

.f1:nth-child(2) {
  background-color: blue;
}

.f1:nth-child(3) {
  background-color: gray;
}

.f1:nth-child(4) {
  background-color: green;
}*/

  .tac {
    text-align: center;
  }

  .tal {
    text-align: left;
  }

  .tar {
    text-align: right;
  }

  .taj {
    text-align: justify;
  }

  .fz44r {
    font-size: 0.44rem;
  }

  .fz4r {
    font-size: 0.4rem;
  }

  .fz36r {
    font-size: 0.36rem;
  }

  .fz32r {
    font-size: 0.32rem;
  }

  .fz24r {
    font-size: 0.24rem;
  }

  .fz2r {
    font-size: 0.2rem;
  }

  /* .popup {
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, .7);
  .MiVideo {
    width: 7.2rem;
    height: 4.05rem;
    height: 3.55rem;
  }
} */

  /* start */

  .p {
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    background: url('../assets/img/p2bg.jpg') no-repeat center top #000;
    background-size: cover;
    .go,
    .next {
      display: block;
      margin: 0 auto;
      width: auto;
      height: 1rem;
    }
  }

  .p:first-child {
    background: url('../assets/img/p1bg.jpg') no-repeat center top #000;
    background-size: cover;
  }

  .p1 {
    .loading1 {
      padding-top: 0.2rem;
      img {
        width: 3rem;
      }
      .progressBar {
        position: absolute;
        top: 0.92rem;
        left: 0.5rem;
        height: .1rem;
        width: 2.5rem;
        border-radius: .1rem;
        background: red;
        animation: loadProgress 2s infinite linear;
      }
    }
    .loading2 {
      width: 5rem;
      height: 5rem;
      margin: 0 auto;
      .circle {
        animation: loadCircle 2s infinite linear;
        transform-origin: 50% 50%;
      }
      .logo {
        position: absolute;
        top: 1.3rem;
        left: 1.5rem;
        width: 2rem;
      }
    }
    .txt {
      width: 5rem;
      margin: 0 auto;
      img {
        height: 1.6rem;
        width: auto;
        display: inline-block;
        margin-left: -1rem;
      }
      .dian {
        position: absolute;
        top: .9rem;
        right: 1rem;
      }
      .dotting {
        display: inline-block;
        min-width: .2rem;
        min-height: .2rem;
        box-shadow: .2rem 0#fff, .6rem 0 #fff, 1rem 0 #fff;
        animation: dot 1s infinite step-start both;
        border-radius: 50%;
      }

      .dotting:before {
        content: '...';
      }
      /* IE8 */
      .dotting::before {
        content: '';
      }

      :root .dotting {
        margin-right: .8rem;
      }

    }
  }

  .p2 {
    .p2h {
      /* padding-top: 2rem; */
      width: 5rem;
      margin: 0 auto;
    }
  }

  .p3,
  .p4,
  .p5,
  .p6,
  .p7 {
    img {
      width: 80%;
      margin: 0 auto;
    }
    /* img:first-child {
      padding-top: 1.6rem;
      width: 5rem;
      margin: 0 auto;
    } */
  }

  .p>.option {
    opacity: 0.7;
  }

  .p>.option.on {
    opacity: 1;
    /* animation: suofang 1s infinite linear; */
  }

  .link {
    text-decoration: none;
    position: absolute;
    /* background: red; */
    width: 5rem;
    top: 9.5rem;
    left: 1.4rem;
    /* display: none; */
  }

  .tada {
    animation: tada 1s infinite linear;
    transform-origin: 50% 50%;
  }

  @-webkit-keyframes tada {
    0%,
    100% {
      transform: rotate3d(0, 0, 1, -10deg);
    }
    50% {
      transform: rotate3d(0, 0, 1, 10deg);
    }
  }

  .suofang {
    animation: suofang 2s infinite linear;
  }

  @-webkit-keyframes suofang {
    0%,
    100% {
      transform: scale3d(1, 1, 1);
    }
    50% {
      transform: scale3d(1.05, 1.05, 1.05);
    }
  }

  .flash {
    animation: flash 1s infinite linear;
  }

  @-webkit-keyframes flash {
    0%,
    100% {
      opacity: 1;
    }
    50% {
      opacity: 0;
    }
  }

  /* IE9+,FF,CH,OP,SF */

  @-webkit-keyframes dot {
    25% {
      box-shadow: none;
    }
    50% {
      box-shadow: .2rem 0 #fff;
    }
    75% {
      box-shadow: .2rem 0 #fff, .6rem 0 #fff;
    }
  }

  @-webkit-keyframes loadProgress {
    0% {
      width: 1%;
    }
    100% {
      width: 2.5rem;
    }
  }

  @-webkit-keyframes loadCircle {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }

  /* transition */

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.5s ease-in-out;
  }

  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }
</style>