<template>
  <div>
    <h4>CarName: {{ $route.query.name }}</h4>
    <h3>CarYear: {{ year }}</h3>

    <div class="scroll"></div>
    <h6 id="scroll">Hello from the bottom</h6>
    <div class="scroll"></div>
  </div>
</template>
<script>
export default {
  computed: {
    year() {
      return this.$route.query.year;
    }
  }
}
</script>
<style scoped>
.scroll {
  width: 100px;
  height: 1000px;
  background-color: #ccc;
}
</style>