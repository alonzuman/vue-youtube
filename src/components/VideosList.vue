<template>
  <div>
    <ul>
      <!-- Iterate through recommended vids array -->
      <li v-for="video in videos" v-bind:key="video.id" class="video-card flex">
        <img class="video-card-thumbnail" :src="video.image" alt />
        <div class="video-card-info">
          <h3>{{video.title}}</h3>
          <h4>{{video.username}}</h4>
          <h4>{{video.views}} views • {{video.datePosted}}</h4>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["videos"],
  name: "VideosList"
};
</script>

<style>
.video-card {
  margin-bottom: 16px;
}

.video-card-info {
  padding: 0px 8px;
}

.video-card-thumbnail {
  height: 90px;
  width: 140px;
  object-fit: cover;
}
</style>