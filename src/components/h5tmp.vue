<template>
  <div class="body">
    <div class="p1">
      <h1>111111</h1>
      <img src="../assets/logo.png" alt="">
      <p>
        <span>a</span>
        <span>a</span>
        <span>a</span>
        <span>a</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "h5",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      curPage: 0
    };
  },
  // 在实例初始化之后，数据观测 (data observer) 和 event/watcher 事件配置之前被调用。
  beforeCreate: function() {
    console.log("beforeCreate");
  },
  // 在实例创建完成后被立即调用。在这一步，实例已完成以下的配置：数据观测 (data observer)，属性和方法的运算，watch/event 事件回调。然而，挂载阶段还没开始，$el 属性目前不可见。
  created: function() {
    console.log("created");
    const self = this;
  },
  // 以下钩子在服务器端渲染期间不被调用。
  // 在挂载开始之前被调用：相关的 render 函数首次被调用。
  beforeMount: function() {
    console.log("beforeMount");
  },
  // el 被新创建的 vm.$el 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，当 mounted 被调用时 vm.$el 也在文档内。
  mounted: function() {
    console.log("mounted");
    // 注意 mounted 不会承诺所有的子组件也都一起被挂载。如果你希望等到整个视图都渲染完毕，可以用 vm.$nextTick 替换掉 mounted：
    this.$nextTick(function() {
      // Code that will run only after the
      // entire view has been rendered
    });
  },
  beforeUpdate: function() {
    console.log("beforeUpdate");
  },
  updated: function() {
    console.log("updated");
  },
  activated: function() {
    console.log("activated");
  },
  deactivated: function() {
    console.log("deactivated");
  },
  beforeDestroy: function() {
    console.log("beforeDestroy");
  },
  destroyed: function() {
    console.log("destroyed");
  },
  errorCaptured: function() {
    console.log("errorCaptured");
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="postcss" scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
p {
  background: red;
  span {
    background: green;
  }
}
</style>
