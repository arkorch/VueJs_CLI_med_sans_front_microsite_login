<template>
  <section id="app">
    <nav class="navbar navbar-inverse">
      <div class="container-fluid">
        <div class="navbar-header">
          <button
            type="button"
            class="navbar-toggle"
            data-toggle="collapse"
            data-target="#myNavbar"
          >
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="#">AB RESISTANCE</a>
        </div>
        <div class="collapse navbar-collapse" id="myNavbar">
          <ul class="nav navbar-nav">
            <li><a href="#" @click="goToHome">Home</a></li>
            <li><a href="#" @click="goToChat">About</a></li>
            <li><a href="#" @click="goToChallenge">Challenge</a></li>
            <li><a href="#" @click="goToInfo">Information</a></li>
          </ul>
          <ul class="nav navbar-nav navbar-right">
            <li>
              <a href="#" @click="goToSignup"
                ><span class="glyphicon glyphicon-user"></span> Sign Up</a
              >
            </li>
            <li>
              <a href="#" @click="goToLogin"
                ><span class="glyphicon glyphicon-log-in"></span> Login</a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- the router view is the container that accepts components to render per route -->
    <router-view></router-view>
    <!-- Footer -->
    <footer class="text-center">
      <!-- Copyright -->
      <div class="text-center p-3 footdiv">
        <p>© 2022 Copyright: Arko | Kanak | Madhur</p>
      </div>
      <!-- Copyright -->
    </footer>
    <!-- Footer -->
  </section>
</template>

<style lang="scss">
@import "@/assets/sass/_vars.scss";
@import "@/assets/sass/_app.scss";
@import "@/assets/sass/_reset.scss";
</style>

<script>
export default {
  methods: {
    goToChat() {
      this.$router.push({ name: "About" });
    },
    goToChallenge() {
      this.$router.push({ name: "Challenge" });
    },
    goToInfo() {
      this.$router.push({ name: "Information" });
    },
    goToSignup() {
      this.$router.push({ name: "Signup" });
    },
    goToLogin() {
      this.$router.push({ name: "Login" });
    },
    goToHome() {
      this.$router.push({ name: "Home" });
    },
  },
};
</script>
