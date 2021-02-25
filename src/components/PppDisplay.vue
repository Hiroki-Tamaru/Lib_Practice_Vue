<template>
  <div class="ppp-display">
    <send-receive-buttons></send-receive-buttons>

    <table class="ppp-table">
      <tr v-for="ppp in pppdata" :key="ppp.id"></tr>
      <tr>
        <td>{{ ppp.id }}</td>
        <td>{{ ppp.PPPname }}</td>
        <td>{{ ppp.AAAname }}</td>
        <td>{{ ppp.CCCname }}</td>
        <td>{{ ppp.RRRname }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "PppDisplay",
  props: {
    pppdata: {
      type: Array,
      required: true,
    },
  },
};
</script>
