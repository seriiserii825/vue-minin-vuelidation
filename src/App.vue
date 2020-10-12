<template>
  <div class="container">
    <h1>Hello world</h1>
    <form>
      <div class="form-group">
        <label for="email">Email</label>
        <input
            type="email"
            id="email"
            class="form-control"
            @input="$v.email.$touch()"
            v-model="email"
        >
      </div>
        <pre>
          {{ $v }}
        </pre>
    </form>
  </div>
</template>

<script>
import {required} from 'vuelidate/lib/validators'

export default {
  name: 'app',
  data() {
    return {
      email: ''
    }
  },
  validations: {
    email: {
      required
    }
  }
}
</script>