<template>
  <div class="container">
    <h1>Hello world</h1>
    <form>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" class="form-control">
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      input: ''
    }
  }
}
</script>