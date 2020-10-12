<template>
  <div>
    <h1>Cars</h1>
    <ul>
      <router-link
          v-for="car in 5"
          tag="li"
          :to="'/car/' + car"
          :key="car"
      >
        <a>{{ car }}</a>
      </router-link>
    </ul>
  </div>
</template>

<script>

</script>

<style scoped>

</style>
