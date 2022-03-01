<template>
  <div id="title">
    <h1>{{ title }}</h1>
    <h2 @click.shift="clear">Shift+Click and Clear</h2>
  </div>
</template>

<script>
export default {
  props: ["title"],
  data() {
    return {};
  },
  methods: {
    clear() {
      this.$emit("clear");
    },
  },
};
</script>

<style scoped>
#title {
  font-size: 2em;
  color: #42b983;
}
</style>
