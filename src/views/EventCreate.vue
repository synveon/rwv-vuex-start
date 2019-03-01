<template>
  <div>
    <h1>Create Event, {{ user.name }}</h1>
    <span>This event was created by {{ user.id }}</span>
    <p>There are {{ catLength }} categories:</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
    <p>{{ getEventById(2) }}</p>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters(['catLength', 'getEventById']),
    ...mapState(['user', 'categories'])
  }
}
</script>

<style scoped>
</style>
