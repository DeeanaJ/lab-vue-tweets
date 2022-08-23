<template>
  <div className="tweet">
    <ProfileImage :image= "user.image" />
    <div className="body">
      <div className="top">
       <User :user="user"/>

        <Timestamp :timestamp= "timestamp" />
      </div>

      <Message :message= "message"/>
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

