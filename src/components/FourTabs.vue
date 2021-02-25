<template>
  <div class="four-tabs">
    <!-- tabs -->
    <div id="tabs" class="container">
      <div class="tabs">
        <a
          v-on:click="changeTabRequest(1)"
          v-bind:class="[activetab === 1 ? 'active' : '']"
          >PPP</a
        >
        <a
          v-on:click="changeTabRequest(2)"
          v-bind:class="[activetab === 2 ? 'active' : '']"
          >AAA</a
        >
        <a
          v-on:click="changeTabRequest(3)"
          v-bind:class="[activetab === 3 ? 'active' : '']"
          >CCC</a
        >
        <a
          v-on:click="changeTabRequest(4)"
          v-bind:class="[activetab === 4 ? 'active' : '']"
          >TTT</a
        >
      </div>

      <div class="content">
        <div v-if="activetab === 1" class="tabcontent">
          Content for tab PPP
          <!-- <ppp-display :pppdata="pppdata"></ppp-display> -->
        </div>
        <div v-if="activetab === 2" class="tabcontent">Content for tab AAA</div>
        <div v-if="activetab === 3" class="tabcontent">Content for tab CCC</div>
        <div v-if="activetab === 4" class="tabcontent">Content for tab TTT</div>
      </div>
    </div>
  </div>
</template>

<script>
import PppDisplayVue from "./PppDisplay.vue";
export default {
  name: "FourTabs",
  props: {
    activetab: {
      type: Number,
      required: true,
    },
    pppdata: {
      // Do not use capital characters!!
      type: Array,
      required: true,
    },
  },
  components: {
    PppDisplay: PppDisplayVue,
  },
  methods: {
    changeTabRequest(tabId) {
      console.log("sending ChangeTabRequest(" + tabId + ")");
      this.$emit("change-tab", tabId);
      // console.log("I am FourTabs.js PPPData is:");
      // console.log(this.pppdata);
    },
  },
};
</script>


<style scoped>
/* tabs */
/* RESET */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 620px;
  min-width: 420px;
  margin: 40px auto;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 0.9em;
  color: #888;
}

/* Style the tabs */
.tabs {
  overflow: hidden;
  margin-left: 20px;
  margin-bottom: -2px;
}

.tabs ul {
  list-style-type: none;
  margin-left: 20px;
}

.tabs a {
  float: left;
  cursor: pointer;
  padding: 12px 24px;
  transition: background-color 0.2s;
  border: 1px solid #ccc;
  border-right: none;
  background-color: #f1f1f1;
  border-radius: 10px 10px 0 0;
  font-weight: bold;
}
.tabs a:last-child {
  border-right: 1px solid #ccc;
}

/* Change background color of tabs on hover */
.tabs a:hover {
  background-color: #aaa;
  color: #fff;
}

/* Styling for active tab */
.tabs a.active {
  background-color: #fff;
  color: #484848;
  border-bottom: 2px solid #fff;
  cursor: default;
}

/* Style the tab content */
.tabcontent {
  padding: 30px;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 3px 3px 6px #e1e1e1;
}
</style>