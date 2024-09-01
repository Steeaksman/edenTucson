<template>
    <div>
      <video
        ref="videoPlayer"
        class="video-js vjs-default-skin"
        controls
        preload="auto"
        width="640"
    height="264"
        :data-setup="{}"
      >
        <source :src="videoSrc" type="video/mp4" />
        Your browser does not support the video tag.
      </video>
    </div>
  </template>
  
  <script setup>
  import { onMounted, ref, watch } from 'vue';
  import videojs from 'video.js';
  import 'video.js/dist/video-js.css';
  
  const props = defineProps({
    videoSrc: {
      type: String,
      required: true,
    },
  });
  
  const videoPlayer = ref(null);
  let player = null;
  
  onMounted(() => {
    player = videojs(videoPlayer.value, {}, function onPlayerReady() {
      console.log('Player is ready');
    });
  
    watch(() => props.videoSrc, (newSrc) => {
      player.src(newSrc);
    });
  });
  
  onBeforeUnmount(() => {
    if (player) {
      player.dispose();
    }
  });
  </script>
  
  <style scoped>
.video-js {
  width: 900px;
  height: 500px;
}
</style>
  