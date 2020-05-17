<template>
  <div>
    <ul>
      <!-- Iterate through comments  -->
      <li v-for="comment in comments" v-bind:key="comment.id" class="comment-card flex">
        <img :src="comment.avatar" alt="#" class="avatar margin-top" />

        <div class="container">
          <h3>{{comment.user}}</h3>
          <h4>{{comment.datePosted}}</h4>
          <p>{{comment.content}}</p>
          <div class="buttons flex">
            <button class="icon-button">
              <i class="fas fa-thumbs-up"></i>
            </button>
            <button class="icon-button">
              <i class="fas fa-thumbs-down"></i>
            </button>
            <button class="icon-button">Reply</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["comments"],
  name: "CommentsSection"
};
</script>

<style>
.margin-top {
  margin-top: 16px;
}

.buttons {
  margin-top: 8px;
}
</style>