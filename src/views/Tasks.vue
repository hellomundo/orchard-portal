<template>
  <div class="section o-page">
      <div class="container">
        <div class="o-part">
            <h1 class="title">Hi Ed!</h1>
            <h3 class="subtitle">Thanks for keeping track of your hours!</h3>
        </div>
      </div>
    <TaskForm />
  </div>
</template>

<script>
// @ is an alias to /src
import TaskForm from '@/components/TaskForm.vue'

export default {
  name: 'task-form',
  components: {
    TaskForm
  }
}
</script>
