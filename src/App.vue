<template>
  <div id="app">
    <vue-uploaders
      :showList="showList"
      :limit="9"
      :listStyle="listStyle"
      :deleStyle="deleStyle"
      :inputStyle="inputStyle"
      :compressPercent="0.3"
      :actionUrl="actionUrl"
      :accept="accept"
      @uploadSuccess="uploadSuccess"
      @uploadError="uploadError"
      @deleteImages="deleteImages">
    </vue-uploaders>
  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      showList: true,
      listStyle: {},
      deleStyle: {},
      inputStyle: {},
      accept: "image/jpg,image/jpeg,image/png,image/gif",
      actionUrl: ''
    }
  },
  methods: {
    uploadSuccess(res) {},
    uploadError(err) {},
    deleteImages(index) {
      console.log(`当前点击删除的图片序号是${index}`);
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
body{
  margin: 0;
}
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
