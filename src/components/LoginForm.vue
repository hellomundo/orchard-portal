<template>
    <div class="columns has-text-centered">
        <div class="column is-6 is-offset-3">
            <h3 class="title is-3">Sign in to the Orchard Parent Portal</h3>
            <form>
                <div class="field has-text-left">
                <label class="label">Email</label>
                <div class="control has-icons-left has-icons-right">
                    <input class="input is-danger is-large" type="email" placeholder="Email input" v-model="email">
                    <span class="icon is-small is-left">
                    <i class="fas fa-envelope"></i>
                    </span>
                    <span class="icon is-small is-right">
                    <i class="fas fa-exclamation-triangle"></i>
                    </span>
                </div>
                <p class="help is-danger">This email is invalid</p>
                </div>
                <div class="field has-text-left">
                <label class="label">Password</label>
                <div class="control has-icons-left">
                    <input class="input is-danger is-large" type="password" placeholder="Password" v-model="password">
                    <span class="icon is-small is-left">
                    <i class="fas fa-key"></i>
                    </span>
                </div>
                <p class="help is-danger">This email is invalid</p>
                </div>
                <div class="control">
                <button class="button is-link is-large">Submit</button>
                </div>
            </form>
        </div>
    </div>
</template>

<script>

export default {
  name: 'LoginForm',
  data: function () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    sayHello: function () {
      return 'hello'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
