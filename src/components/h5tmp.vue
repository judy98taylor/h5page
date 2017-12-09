<template>
  <div class="body">

    <transition name="fade">
      <div class="p p1" v-show="curPage==1">
        <h1>1111100001</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p2" v-show="curPage==2">
        <h1>22222</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p3" v-show="curPage==3">
        <h1>3333333</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p4" v-show="curPage==4">
        <h1>444444</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p5" v-show="curPage==5">
        <h1>5555555</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p6" v-show="curPage==6">
        <h1>666666</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p7" v-show="curPage==7">
        <h1>7777777</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p8" v-show="curPage==8">
        <h1>88888888888888</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p9" v-show="curPage==9">
        <h1>999999999</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p10" v-show="curPage==10">
        <h1>7777777</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p11" v-show="curPage==11">
        <h1>88888888888888</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
      </div>
    </transition>

    <transition name="fade">
      <div class="p p12" v-show="curPage==12">
        <h1>999999999</h1>
        <img src="../assets/666.gif" alt="">
        <p>
          <span>a</span>
          <span>a</span>
          <span>a</span>
          <span>a</span>
        </p>
        <button @click="next()">next</button>
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
      msg: "Welcome to Your Vue.js App",
      // curPage: 0,
      curPage: 1
    };
  },
  // 在实例初始化之后，数据观测 (data observer) 和 event/watcher 事件配置之前被调用。
  beforeCreate: function() {
    // console.log("beforeCreate");
  },
  // 在实例创建完成后被立即调用。在这一步，实例已完成以下的配置：数据观测 (data observer)，属性和方法的运算，watch/event 事件回调。然而，挂载阶段还没开始，$el 属性目前不可见。
  created: function() {
    // console.log("created");
  },
  // 以下钩子在服务器端渲染期间不被调用。
  // 在挂载开始之前被调用：相关的 render 函数首次被调用。
  beforeMount: function() {
    // console.log("beforeMount");
  },
  // el 被新创建的 vm.$el 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，当 mounted 被调用时 vm.$el 也在文档内。
  mounted: function() {
    // console.log("mounted");

    // // 注意 mounted 不会承诺所有的子组件也都一起被挂载。如果你希望等到整个视图都渲染完毕，可以用 vm.$nextTick 替换掉 mounted：
    // this.$nextTick(function() {
    //   // Code that will run only after the
    //   // entire view has been rendered
    // });

    const self = this;
    var a = () => {
      console.log("fn");
    };
    a();
    $("p").addClass("sp");

    // $.get("", {}, function(data, status, xhr) {});
  },
  // beforeUpdate: function() {
  //   console.log("beforeUpdate");
  // },
  // updated: function() {
  //   console.log("updated");
  // },
  // activated: function() {
  //   console.log("activated");
  // },
  // deactivated: function() {
  //   console.log("deactivated");
  // },
  // beforeDestroy: function() {
  //   console.log("beforeDestroy");
  // },
  // destroyed: function() {
  //   console.log("destroyed");
  // },
  // errorCaptured: function() {
  //   console.log("errorCaptured");
  // }
  methods: {
    next: function() {
      const self = this;
      self.curPage++;
      self.curPage =
        self.curPage % 12 > 0 && self.curPage % 12 < 8 ? self.curPage % 12 : 1;
    }
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
  transition: transform 1s;
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

p {
  background: red;
  font-size: 1rem;

  span {
    background: green;
    font-size: 0.4rem;
  }

  display: flex;
}

/* start */
.p {
  width: 100vw;
  height: 100vh;
}

.p:nth-child(2n) {
  background: aqua;
}

/* transition */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
