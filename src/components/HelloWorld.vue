<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="user in users" :key="user.id">{{ user.first_name }}</li>
    </ul>
  </div>
</template>

<script>
import sourcedata from '@/data'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function () {
    return {
      families: sourcedata.families,
      users: sourcedata.users
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
