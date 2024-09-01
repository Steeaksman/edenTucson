<template>
    <div class="flex flex-col items-center p-8 h-screen bg-gray-800">
      <h1>Nuxt 3 Video.js Player</h1>
      <VideoJsPlayer videoSrc="https://s3.us-west-1.amazonaws.com/stonetigermedia.com/Bearologist!.mp4" />
      <!-- <VideoJsPlayer videoSrc="https://s3.us-west-1.amazonaws.com/stonetigermedia.com/Lingus.mp4  "/> -->
    </div>
  </template>
  
  <script setup>
  import VideoJsPlayer from '~/components/VideoJsPlayer.vue';
  </script>
  