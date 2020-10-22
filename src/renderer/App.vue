<template>
    <div id="app">
        {{name}}
        <div>
            <button @click="get_company_name">click</button>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'app',
    data () {
      return {
        name: 'default'
      }
    },
    methods: {
      get_company_name: function () {
        var company = require('./sdk/company')
        if (this.name === 'default') {
          this.name = company.get_name()
        } else {
          this.name = 'default'
        }
      }
    }
  }
</script>

<style>
    /* CSS */
</style>
