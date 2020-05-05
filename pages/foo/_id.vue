<template>
  <div class="container">
    Page ID: {{ id }}

    <hr />

    <NuxtLink :to="{ name: 'foo-id', params: { id: id + 1 } }">Next Page</NuxtLink>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      id: Number,
    }
  },
  asyncData({ params }) {
    console.log('asyncData')

    return {
      id: Number(params.id)
    }
  },
  beforeRouteUpdate(to, from, next) {
    console.log('beforeRouteUpdate')
    next()
  },
})
</script>