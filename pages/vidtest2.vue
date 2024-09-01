<template>
    <div>
      <h1>Nuxt 3 Video.js Player</h1>
      <!-- <VideoJsPlayer videoSrc="https://s3.us-west-1.amazonaws.com/stonetigermedia.com/Bearologist!.mp4" /> -->
      <VideoJsPlayer videoSrc="https://vjs.zencdn.net/8.10.0/video.min.js" />
    </div>
  </template>
  
  <script setup>
  import VideoJsPlayer from '~/components/VideoJsPlayer.vue';
  </script>
  