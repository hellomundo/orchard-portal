<template>
  <div class="container">
    <section class="section">
      <div class="columns">
        <div class="column has-text-centered">
          <h1 class="is-size-3 has-text-weight-bold">{{ family.name }}</h1>
          <p class="is-size-5">Family Account</p>
        </div>
      </div>
    </section>
   <section class="section">
      <div class="columns">
        <div class="column is-mobile is-primary has-text-centered">
          <h2 class="is-size-6 is-uppercase">Balance</h2>
          <p class="key-stat is-size-1">{{ family.balance | make_currency }}</p>
          <p><a class="button key-button is-primary is-large is-uppercase has-text-weight-bold">Pay Now</a></p>
          <a class="button is-clear is-uppercase is-small has-text-weight-bold is-borderless">See details</a>
        </div>
      </div>
    </section>
    <section class="section">
      <ActivityList :family="family"/>
    </section>
    <section class="section light-green-background">
        <div class="columns">
          <div class="column is-mobile is-primary has-text-centered">
            <h2 class="is-size-6 is-uppercase">Hours</h2>
            <p class="key-stat is-size-1">45 / 52</p>
            <p><router-link :to="'/tasks'" class="button key-button is-primary is-large is-uppercase has-text-weight-bold">Add Hours</router-link></p>
            <a class="button is-clear is-uppercase is-small has-text-weight-bold is-borderless is-clear">See details</a>
          </div>
        </div>
      </section>
   </div>
</template>

<script>
// @ is an alias to /src
import sourcedata from '@/data'
import ActivityList from '@/components/ActivityList.vue'

export default {
  name: 'home',
  components: {
    ActivityList
  },
  data: function () {
    return {
      family: sourcedata.families[0]
    }
  },
  filters: {
    make_currency: function (value) {
      return new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD' }).format(value)
    }
  }
}
</script>

<style>
  .info-pane {
    padding: 1em;
    background-color: #ddd;
  }
</style>
