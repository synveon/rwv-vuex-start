<template>
  <div>
    <h1>Create Event, {{ user.name }}</h1>
    <p>This event was crated by {{ user.id }}</p>
    <p>There are {{ catLength }} categories</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
    <p>{{ getTodoById(1) }}</p>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters(['catLength', 'getTodoById']),
    ...mapState(['user', 'categories'])
  }
}
</script>

<style scoped>
</style>