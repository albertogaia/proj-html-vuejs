<template>
  <div class="chat-box">
    <div class="chat-top">
      <div class="img-chat">
        <img src="https://randomuser.me/api/portraits/men/47.jpg" alt="" />
      </div>
      <span class="header-chat montserrat"
        >Alberto
        <p>Assistenza clienti</p></span
      >
    </div>
    <div class="chat-bottom">
      <div class="chat-body">
        <div class="msg msg-received">
          <p>Benvenuto su Phlox! Come possiamo aiutarti?</p>
        </div>
        <div
          v-for="(msg, index) in arraymsg"
          :key="index"
          v-bind:class="msg.status == 'sent' ? 'msg-sent' : 'msg-received'"
          class="msg"
        >
          {{ msg.text }}
        </div>
      </div>
      <div class="chat-input">
        <input
          type="text"
          placeholder="Come possiamo aiutarti?"
          v-model="inputText"
          @keyup.enter="getMessage"
          id="input-msg"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Chatbox",
  data() {
    return {
      inputText: "",
      arraymsg: [],
      msgReceived: {
        text: "Al momento siamo offline, ci dispiace!",
        status: "received",
      },
    };
  },

  methods: {
    getMessage() {
      let msg = this.inputText;

      let msgObj = {
        text: msg,
        status: "sent",
      };

      if (msg != "") {
        this.arraymsg.push(msgObj);
      }
      this.inputText = "";
      setTimeout(this.receiveMsg, 1000);
    },

    receiveMsg() {
      this.arraymsg.push(this.msgReceived);
      document.getElementById("input-msg").disabled = true;
    },
  },
  mounted() {
    this.getMessage;
  },
};
</script>
<style lang="scss" scoped>
@import "../../styles/general.scss";

.chat-box {
  width: 20%;
  height: 50%;
  background-color: $white;
  border-radius: 15px 15px 0 15px;
  position: fixed;
  right: 60px;
  bottom: 100px;
  overflow: hidden;
  box-shadow: 3px 3px 10px rgba($dark-blue, 0.2);

  .chat-top {
    padding: 15px;
    height: 80px;
    box-shadow: 0px 3px 50px rgba($dark-blue, 0.2);
    display: flex;
    align-items: center;
    background-color: $dark-secondary;
    color: $white;
    .img-chat {
      display: inline-block;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      overflow: hidden;
      img {
        object-fit: cover;
        object-position: center;
        width: 100%;
      }
    }
    span.header-chat {
      margin-left: 15px;
      font-weight: $bold;
      p {
        font-weight: $regular;
        font-size: $fs-small;
      }
    }
  }
  .chat-bottom {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: calc(100% - 80px);
    .chat-body {
      width: 100%;
      height: calc(100% - 50px);
      display: flex;
      flex-direction: column;
      .msg {
        padding: 10px 25px;
        display: inline-block;
        margin: 5px;
        width: max-content;
        max-width: 70%;
        font-family: $montserrat;
        font-size: 14px;
        font-weight: $regular;
        color: $white;
      }
      .msg-sent {
        align-self: flex-end;
        background-color: $blue;
        color: $white;
        border-radius: 5px 5px 0 5px;
      }
      .msg-received {
        align-self: flex-start;
        background-color: rgba($dark-blue, 0.9);
        border-radius: 5px 5px 5px 0px;
      }
    }
    .chat-input {
      width: 100%;
      height: 50px;
      position: absolute;
      bottom: 0;
      input {
        height: 100%;
        width: 100%;
        padding-left: 20px;
        outline: none;
        border: none;
        box-shadow: 0px -3px 40px rgba($dark-blue, 0.2);
        font-size: $fs-p;
      }
    }
  }
}
</style>