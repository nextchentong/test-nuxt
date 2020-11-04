<template>
  <div class="container">
    <div>
      <Logo style="margin-bottom:20px"/>
      <Alert :show="show" @closealert="closeAlert" st/>
      <el-button type="primary" @click="clickBtn">点击弹出对话框</el-button>
      <div class="links"></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    };
  },
  methods: {
    clickBtn() {
      this.show = true;
    },
    closeAlert(type) {
      console.log("监听到了");
      this.show = type;
    },
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
