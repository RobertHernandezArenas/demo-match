<template>
  <div id="app">
    <hls-player
      :width="900"
      :height="500"
      :autoplay="true"
      :muted="true"
      :controls="true"
      ref="myPlayer"
      :source="src"
    />
    <h2 class="ad">
      ---Esta retransmición es sin animo de lucro y con fines de auditoria personal---
    </h2>
  </div>
</template>

<script>
import "hls-player/dist/hls-player.css";
import hlsPlayer from "hls-player";

export default {
  name: "App",
  components: {
    hlsPlayer,
  },
  data() {
    return {
      src: "http://51.161.115.48:8080/live/tito_robert/ZpAzL2e7FK/23517.m3u8",
    };
  },
};
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
