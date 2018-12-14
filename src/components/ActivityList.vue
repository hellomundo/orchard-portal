<template>
  <div>
    <table class="table is-fullwidth ">
        <thead>
            <th>Date</th>
            <th>Name</th>
            <th class="has-text-centered">Activity</th>
            <th class="has-text-centered">Qty</th>
            <th class="has-text-right">Amount</th>
            <th class="has-text-centered">Status</th>
        </thead>
        <tr v-for="activity in fam.activities" :key="activity.id">
            <td>{{ activity.date }}</td>
            <td>{{ activity.name }}</td>
            <td class="has-text-centered">{{ activity.act }}</td>
            <td class="has-text-centered">{{ activity.quantity }}</td>
            <td class="has-text-right">{{ activity.amount }}</td>
            <td class="has-text-centered"><span class="tag">UNPAID</span></td>
        </tr>
    </table>
  </div>
</template>

<script>

export default {
  name: 'ActivityList',
  props: {
    family: Object
  },
  data: function () {
    return {
      fam: this.family
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
