<template>
  <div>
    <!--_________HERO START_________ -->
    <div class="container">
      <div class="row">
        <div class="col-sm-7 first-column">
          <img src="../assets/images/Poster_5.jpg" />
        </div>
        <div class="col-sm-5 second-column text-left">
          <h4>The AB Free Challenge</h4>
          <p>Login to checkout new updates!</p>
          <br /><br />
          <section class="log-in">
            <label class="sr-only" for="inlineFormInputName">Name</label>
            <input
              v-model="username"
              type="text"
              class="form-control"
              id="inlineFormInputName"
              placeholder="Name"
              required
            />
            <label class="sr-only" for="inlineFormInputName">Name</label>
            <input
              v-model="username"
              type="text"
              class="form-control"
              id="inlineFormInputName"
              placeholder="Contact Number"
              required
            />

            <label class="sr-only" for="inlineFormInputName">Name</label>
            <input
              v-model="username"
              type="text"
              class="form-control"
              id="inlineFormInputName"
              placeholder="Username"
              required
            />

            <label class="sr-only" for="inlineFormPassword">Name</label>
            <input
              v-model="password"
              type="password"
              class="form-control"
              id="inlineFormPassword"
              placeholder="Password"
              required
            />
            <input
              v-model="password"
              type="password"
              class="form-control"
              id="inlineFormPassword"
              placeholder="Confirm password"
              required
            />
            <div class="controls">
              <button :class="{ disabled: canJoin }" :disabled="canJoin" @click="goToHome">
                Login!
              </button>
            </div>
          </section>
        </div>
      </div>
      <br /><br /><br /><br />
    </div>

    <!--_________HERO END_________ -->
  </div>
</template>

<style lang="scss">
@import "@/assets/sass/_vars.scss";
@import "@/assets/sass/_login.scss";
@import "@/assets/sass/_reset.scss";
</style>

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
    goToHome() {
      this.$router.push({ name: "Home", params: { ChatUserName: this.username || "Mr.No Name" } });
    },
  },
};
</script>
