<template>
    <div class="o-part">
        <div class="notification is-primary">
            <button class="delete"></button>
                Awesome! Thanks for contributing those hours! Look below the form to see where you stand.
        </div>
        <form>
            <div class="columns is-mobile">
                <div class="column">
                    <div class="field">
                        <label class="label">What did you do?</label>
                        <div class="control">
                            <div class="select is-large">
                                <select>
                                    <option>Select a task</option>
                                    <option>With options</option>
                                </select>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="column">
                    <div class="field">
                        <label class="label">Hours</label>
                        <div class="control">
                            <input class="input is-large" type="text" placeholder="1.25">
                        </div>
                        <p class="help">How many hours did you contribute. Can be decimal like "1.5".</p>
                    </div>
                </div>
            </div>
            <div class="columns">
                <div class="column">
                    <div class="field">
                        <label class="label">Performed on</label>
                        <div class="control">
                            <DatePicker input-class="input is-large" :typeable="true" placeholder="When you did it" v-model="performed_on" />
                        </div>
                        <p class="help">Date that you perfomed the task.</p>
                    </div>
                </div>
            </div>
            <div class="columns">
                <div class="column">
                    <div class="field">
                        <label class="label">Notes (optional)</label>
                        <div class="control">
                            <textarea class="textarea is-large" placeholder="Your notes go here."></textarea>
                        </div>
                    </div>
                </div>
            </div>
            <div class="field">
                <div class="control">
                    <button class="button is-primary is-large">Submit</button>
                </div>
            </div>
        </form>
    </div>
</template>

<script>
import DatePicker from 'vuejs-datepicker'

export default {
  name: 'TaskForm',
  components: {
    DatePicker
  },
  data: function () {
    return {
      task_id: '',
      hours: '',
      performed_on: new Date(),
      notes: '',
      task_types: [{
        task_id: 1,
        task_name: 'Parent Meeting'
      }, {
        task_id: 2,
        task_name: 'Animal Care'
      }
      ]
    }
  },
  methods: {
    submitTaskHours: function () {
      return 'hello'
    }
  }
}
</script>

<style>
</style>
