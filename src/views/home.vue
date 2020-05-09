<template>
  <div class="home">
    <button @click="clickHandle">switch</button>
    <iframe :src="src" ref="iframe" frameborder="0"></iframe>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      src: './static/blog.html'
    }
  },
  methods: {
    clickHandle () {
      // 切换路径促使切换数据
      this.src = '../../static/second.html'
    }
  }
}
</script>

<style>
iframe {
  width: 800px;
  height: 100vh;
  margin: 0 auto;
  display: block;
}
button {
  position: fixed;
  left: calc(50% - 450px);
  top: 50px;
  border: 1px solid #cccccc;
  background-color: #ffffff;
  border-radius: 3px;
  padding: 3px 5px;
  cursor: pointer;
}
</style>
