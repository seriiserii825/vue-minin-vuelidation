<template>
  <div>
    <h1>Car id: {{ id }}</h1>
    <button @click="goBackToCars" class="btn btn-primary">Go back</button>
    <router-link
        tag="button"
        class="btn btn-success"
        :to="{name: 'carFull', params: {id: id}, query: {
          name: 'Mazda',
          year: 2020
        }, hash: '#scroll'}"
    >Info</router-link>
    <hr>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  data() {
    return {
      id: this.$router.currentRoute.params['id']
    }
  },
  methods: {
    goBackToCars(){
      this.$router.push('/cars')
    }
  },
  watch: {
    $route(toR, fromR) {
      this.id = toR.params['id']
    }
  }
}
</script>