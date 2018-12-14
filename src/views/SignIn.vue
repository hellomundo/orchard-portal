<template>
  <div class="section">
    <LoginForm />
  </div>
</template>

<script>
// @ is an alias to /src
import LoginForm from '@/components/LoginForm.vue'

export default {
  name: 'signin',
  components: {
    LoginForm
  }
}
</script>
