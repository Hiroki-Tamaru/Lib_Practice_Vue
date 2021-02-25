<template>
  <div class="upper-components">
    <!-- Product logo -->
    <img src="../assets/logo.png" alt="ロゴ" />

    <!-- descriptor -->
    <div class="descriptor">
      <p>User 001</p>
      <p>User PPP001</p>
    </div>

    <button class="button" v-on:click="sendAllOfR">Send</button>

    <button class="button" v-on:click="receiveAllOfR">Receive</button>
  </div>
</template>