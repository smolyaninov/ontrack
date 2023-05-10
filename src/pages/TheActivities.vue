<script setup>
import { validateActivities } from '../validators'
import ActivityItem from '../components/ActivityItem.vue'

defineProps({
  activities: {
    requierd: true,
    type: Array,
    validate: validateActivities
  }
})
</script>

<template>
  <div>
    <ul class="divide-y">
      <ActivityItem v-for="activity in activities" :key="activity" :activity="activity" />
    </ul>
  </div>
</template>
