<template>
  <div class="video-details">
    <iframe
      width="100%"
      height="400px"
      src="https://www.youtube.com/embed/JLc-hWsPTUY"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
    <h2>{{video.title}}</h2>
    <div class="info-and-controlls">
      <h4>{{video.views}} views • {{video.datePosted}}</h4>
      <div class="controlls">
        <button class="icon-button">
          <i class="fas fa-thumbs-up"></i>
        </button>
        <button class="icon-button">
          <i class="fas fa-thumbs-down"></i>
        </button>
        <button class="icon-button">
          <i class="fas fa-share"></i>
        </button>
        <button class="icon-button">
          <i class="fas fa-bookmark"></i>
        </button>
        <button class="icon-button">
          <i class="fas fa-ellipsis-h"></i>
        </button>
      </div>
    </div>

    <div class="avatar-and-info">
      <div class="flex info-header">
        <div class="flex">
          <img
            src="https://yt3.ggpht.com/a/AATXAJymAoabJmVZ9GJxk31TauUl3MEMOpJIgpYwlg=s88-c-k-c0xffffffff-no-rj-mo"
            alt="#"
            class="avatar"
          />
          <div class="user-and-video-info">
            <h3>{{video.user.name}}</h3>
            <h5>{{video.user.subscribers}} subscribers</h5>
          </div>
        </div>
        <div>
          <button v-on:click="subscribeToUser" v-if="!subscribed" class="subscribe-button">SUBSCRIBE</button>
          <button v-on:click="unsubscribeToUser" v-else class="ubsubscribe-button">UNSUBSCRIBE</button>
        </div>
      </div>

      <div class="video-description">
        <p>{{video.description}}</p>
      </div>
    </div>
    <CommentsSection v-bind:comments="video.comments"></CommentsSection>
  </div>
</template>

<script>
import CommentsSection from "./CommentsSection.vue";

export default {
  props: ["video"],
  name: "VideoDetails",
  components: { CommentsSection },
  data() {
    return {
      subscribed: false
    };
  },
  methods: {
    subscribeToUser() {
      this.subscribed = true;
    },
    unsubscribeToUser() {
      this.subscribed = false;
    }
  }
};
</script>

<style>
.info-and-controlls {
  display: flex;
  justify-content: space-between;
}

.controlls {
  margin-top: 16px;
}

.info-header {
  justify-content: space-between;
}

.avatar {
  height: 40px;
  width: 40px;
  object-fit: cover;
  border-radius: 50%;
}

.avatar-and-info {
  padding: 16px 0px;
  border-top: var(--border);
  border-bottom: var(--border);
}

.user-and-video-info {
  padding: 0px 16px;
}

.subscribe-button {
  border: 1px solid var(--red);
  border-radius: 2px;
  background-color: var(--red);
  color: white;
  margin-top: 0;
}

.subscribe-button:focus {
  outline: none;
}

.unsubscribe-button {
  border: none;
  border-radius: 2px;
  background-color: var(--inactive);
  color: white;
  margin-top: 0;
}

.video-description {
  margin-left: 40px;
  padding-left: 16px;
  padding-right: 16px;
  padding-top: 8px;
}
</style>
