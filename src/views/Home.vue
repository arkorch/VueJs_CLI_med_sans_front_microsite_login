<template>
  <section id="welcome-wrapper">
    <h1 class="hidden">Sign In</h1>
    <h2>Welcome to the Chat App</h2>

    <input type="text" name="username" v-model="username" placeholder="Type your Name here" />

    <div class="controls">
      <button :class="{ disabled: canJoin }" :disabled="canJoin" @click="goToChat">
        Joinnnnnn Chat!
      </button>

      <button @click="goToChat">Join Annonymously</button>
      <button>
        <i class="fa fa-paper-plane mybutton" aria-hidden="true"></i>
      </button>
    </div>
  </section>
</template>
<script>
export default {
  name: "LoginPage",

  data() {
    return {
      loggedIn: false,
      username: "",
    };
  },

  computed: {
    canJoin: function () {
      return this.username.trim() === "";
    },
  },

  methods: {
    goToChat() {
      this.$router.push({ name: "Chat", params: { ChatUserName: this.username || "Mr.No Name" } });
    },
  },
};
</script>
<style lang="scss">
@import "@/assets/sass/_vars.scss";
@import "@/assets/sass/_home.scss";
@import "@/assets/sass/_reset.scss";
</style>
