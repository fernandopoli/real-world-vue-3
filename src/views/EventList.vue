<template>
  <div class="events">
    <h2>Events for Good</h2>
    <EventCard v-for="(event, index) in events" :key="index" :event="event" />
  </div>
</template>

<script>
import EventService from '@/services/EventService.js'
import EventCard from '@/components/EventCard.vue'

export default {
  name: 'EventList',
  components: {
    EventCard,
  },
  data() {
    return {
      events: null,
    }
  },
  created() {
    EventService.getEvents()
      .then((response) => {
        this.events = response.data
      })
      .catch((error) => {
        console.log(error)
      })
  },
}
</script>
<style scoped lang="scss">
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
