<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 in CodeSandbox" /> -->
  <!-- <test-component msg="Konnichiwa" :num="1" /> -->

  <upper-components></upper-components>
  <four-tabs
    :activetab="activetab"
    :pppdata="PPPData"
    @change-tab="changeTab"
  ></four-tabs>
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
import TestComponentVue from "./components/TestComponent.vue";
import FourTabsVue from "./components/FourTabs.vue";
import SendReceiveButtonsVue from "./components/SendReceiveButtons.vue";
import UpperComponentsVue from "./components/UpperComponents.vue";
export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
    TestComponent: TestComponentVue,
    FourTabs: FourTabsVue,
    SendReceiveButtons: SendReceiveButtonsVue,
    UpperComponents: UpperComponentsVue,
  },
  data() {
    return {
      activetab: 1,
      PPPData: [
        {
          id: 1,
          PPPname: "User PPP 001",
          AAAname: "AAA 001",
          CCCname: "CCC 001",
          RRRname: "RRR1",
        },
        {
          id: 2,
          PPPname: "User PPP 002",
          AAAname: "AAA 002",
          CCCname: "CCC 002",
          RRRname: "RRR2",
        },
        {
          id: 3,
          PPPname: "User PPP 003",
          AAAname: "AAA 003",
          CCCname: "CCC 003",
          RRRname: "RRR3",
        },
      ],
    };
  },
  methods: {
    changeTab(tabId) {
      this.activetab = tabId;
      console.log("Changing Tab to " + tabId);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
