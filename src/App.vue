<template>
  <div id="app">
    <div v-for="(item, i) in videoList" :key="i">
      <VideoJS :src="item.videoUrl" :type="item.type" :id="i" />
    </div>
  </div>
</template>

<script>
import VideoJS from "./components/VideoPlayer.vue";

export default {
  name: "App",
  components: {
    VideoJS,
  },
  data() {
    return {
      videoList: [
        {
          videoUrl:
            "https://ov-cms.s3.ap-south-1.amazonaws.com/B2B/AdminPanel/CMS/AGY20519/Images/28092020061954.mp4",
          type: "video/mp4",
        },
        {
          videoUrl: "https://www.youtube.com/watch?v=DH1tVM4yOcU",
          type: "video/youtube",
        },
        {
          videoUrl: "https://www.youtube.com/watch?v=3OhLUYNw0TI",
          type: "video/youtube",
        },
        {
          videoUrl: "https://www.youtube.com/watch?v=CQaDl9Fu0W0",
          type: "video/youtube",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
