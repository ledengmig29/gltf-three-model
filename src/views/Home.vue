<template>
  <div id="home">
    <table class="attributes" v-if="isShow">
      
    </table>
  </div>
</template>

<script>
import Viewer from "@/core/viewer.js";

export default {
  name: "Home",
  data() {
    return {
      viewer: null,
      viewerEl: null,
      isShow: false
    }
  },
  mounted() {
    this.viewerEl = document.getElementById("home");
    this.viewer = new Viewer(this.viewerEl);
    this.viewer.load('files/gltf/NewProject.gltf');
  }
};
</script>

<style scoped>
#home {
  width: 100vw;
  height: 100vh;
}
.attributes {
  display: block;
  height: 300px;
  position: absolute;
  right: 10px;
  top: 10px;
  border: 3px solid #aaa;
  border-collapse: collapse;
  overflow-y: scroll;
}
.attributes td {
  height: 30px;
  text-align: center;
  border: 1px solid #aaa;
}
.attributes th {
  height: 30px;
   text-align: center;
   border: 1px solid #aaa;
 }

</style>
