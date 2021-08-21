<template>
  <div class="events">
    <h2>Events for Good</h2>
    <EventCard v-for="(event, index) in events" :key="index" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'

export default {
  name: 'EventList',
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          date: '13/08/1981',
          time: '18:00',
          title: 'Prueba 01',
        },
        {
          date: '13/08/1982',
          time: '18:00',
          title: 'Prueba 02',
        },
        {
          date: '13/08/1983',
          time: '18:00',
          title: 'Prueba 03',
        },
        {
          date: '13/08/1984',
          time: '18:00',
          title: 'Prueba 04',
        },
      ],
    }
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
