<template>
  <div class="PDF-viewer" >
    <h1 :style="textStyle">My Title</h1>
    <p>
      testing pdf
    </p>
    <div id="app">
      <WebViewer :path="`${publicPath}`" url="https://pdftron.s3.amazonaws.com/downloads/pl/webviewer-demo.pdf"/>
    </div>
  </div>
</template>

<script>

import WebViewer from './components/WebViewer.vue'

export default {
  name: 'App',
  components: {
    WebViewer
  },
  data () {
    return {
      publicPath: "/dist/pdfjsexpress/"
    }
  }
}
</script>

<style lang="scss" scoped>
.my-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 200px;
  h1 {
    font-size: 32px;
  }
  p {
    margin-top: 12px;
  }
}
</style>
