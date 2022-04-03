<template>
  <main>
    <h1 class="welcome-message">Welcome {{ ChatUserName }}</h1>
  </main>
</template>

<style lang="scss">
@import "@/assets/sass/_vars.scss";
@import "@/assets/sass/_chat.scss";
@import "@/assets/sass/_reset.scss";
</style>

<script>
// import io from "socket.io-client";
// import vars from "@/env.js";
// import ChatMessage from "@/components/ChatMessage.vue";

export default {
  name: "TheChatComponent",

  props: {
    ChatUserName: String,
  },
};

// export default {
//   name: "TheChatComponent",

//   props: {
//     ChatUserName: String
//   },

//   mounted() {
//     let vm = this;

//     this.socket.on("CONNECTED", (id) => {
//       // debugger;
//       vm.socketID = id;
//     })

//   this.socket.on('MESSAGE', (message) => {
//       // debugger;
//       vm.messages = [...vm.messages, message];
//       console.log(message);
//     })

//     this.socket.on('TEST_FOR_EVENT', (data) => {
//       console.table(data);
//     })

//   },

//   computed: {
//     messageContent: function() {
//       return this.message.trim() === '';
//     }

//   },

//   data() {
//     return {
//       //store the connection ID so we can use it later
//       socketID: '',
//       message: '',
//       messages: [],

//       socket: io(vars.basePath, {
//         withCredentials: false,
//         extraHeaders: {
//           'Access-Control-Allow-Origin': '*'
//         }
//       })
//     }
//   },

//   methods: {
//     sendMessage() {
//       this.socket.emit('SEND_MESSAGE', { user: this.ChatUserName || "Anonymous", message: this.message })

//       this.message = '';
//     },

//     sendOnEnter() {
//       if (this.messageContent == false && event.keyCode == 13) {
//         this.sendMessage();
//       } else {
//         this.socket.emit("TYPING", { user: this.username || "Anonymous" });
//       }
//     }
//   },

//   components: {
//     ChatMessage
//   }
// }
</script>
