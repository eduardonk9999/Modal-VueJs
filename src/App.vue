<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name" />
  <button @click="handleClick">click me</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      title: "My First Vue App :)",
    };
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name);
    },
  },
};
</script>

<style>
</style>
