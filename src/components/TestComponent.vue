<template>
  <div class="test-component"></div>
  <p>This is a test component. prop message is {{ msg }}</p>
  <p>Prop is {{ num }}</p>
</template>

<script>
export default {
  name: "TestComponent",
  props: {
    msg: String,
    num: Number,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p {
  color: green;
}
</style>
