<template>
  <div class="page-layout flex">
    <div class="container left-column">
      <VideoDetails v-bind:video="dummyData.mainVideo"></VideoDetails>
    </div>
    <div class="container">
      <VideosList v-bind:videos="dummyData.videos"></VideosList>
    </div>
  </div>
</template>

<script>
import VideoDetails from "./VideoDetails.vue";
import VideosList from "./VideosList.vue";

export default {
  props: ["dummyData"],
  name: "VideoPage",
  components: { VideoDetails, VideosList }
};
</script>

<style>
.page-layout {
  margin-top: 60px;
}

.container {
  padding: 16px;
}

.flex {
  display: flex;
}

.left-column {
  width: 70%;
}
</style>