<template>
  <router-link
    :to="{ name: 'EventDetail', params: { id: event.id } }"
    class="event-card"
  >
    <span>@ {{ event.time }} on {{ event.date }}</span>
    <h4>{{ event.title }}</h4>
  </router-link>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    event: Object,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.event {
  &-card {
    text-decoration: none;
    color: black;
    margin-bottom: 30px;
    width: 250px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid;
    padding: 30px;
    transition: all 300ms;
    &:hover {
      box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.24);
    }
    h4 {
      margin-bottom: 0px;
    }
  }
}
</style>
