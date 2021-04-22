<template>
  <div id="app"></div>
</template>

<script>
export default {
  async created() {
    await this.$store.dispatch("changeDataAction");
    console.log(this.$store.state.list.data);
  },
};
</script>


<style scoped>
.left {
  width: 22%;
  height: 100vh;
}
.right {
  width: 78%;
  height: 100vh;
}
.flex {
  display: flex;
}
.title {
  border-bottom: 1px solid white;
  border-left: 1px solid white;
  padding: 15px;
}
.title p {
  font-size: 20px;
  font-weight: bold;
}
</style>