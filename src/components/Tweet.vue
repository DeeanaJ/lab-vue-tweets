<template>
  <div className="tweet">
    <ProfileImage :image="user.image" />
    <div className="body">
      <div className="top">
        <span className="user">
          <span className="name">Ironhack</span>
          <span className="handle">@ironhack</span>
        </span>

        <Timestamp :timestamp="timestamp" />
      </div>

      <p className="message">
        On December 7th, we will be hosting a #webinar that will introduce you
        to #SQL! Are you ready? 🚀
      </p>
    <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
<script>
import Timestamp from "./Timestamp.vue";
import Actions from "./Actions.vue";
import ProfileImage from "./ProfileImage.vue";
import Message from "./Message.vue";
import User from "./User.vue"

export default{
  props: {
    user : {
      name: String,
      handle: String,
      image: String,
    },
    timestamp: String,
    message: String,
  },
  components: { Timestamp, Actions, ProfileImage, Message, User},
};
</script>

