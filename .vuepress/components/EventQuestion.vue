<template>
  <section class="talk">
    <div class="type">Q&A</div>
    <h3 class="title">{{ title }}</h3>
    <EventSpeaker :speaker="speaker" />
  </section>
</template>

<script>
export default {
  props: ['title', 'speaker', 'deck', 'issue'],
  filters: {
    filename (value) {
      return value.split('/').pop()
    }
  }
}
</script>

<style scoped>
.talk {
  position: relative;
  border: 1px solid rgba(0, 0, 0, 0.05);
  border-radius: 1rem;
  padding: 1rem;
  box-shadow: 0 4px 10px -4px rgba(0, 0, 0, 0.5);
}
.talk:hover {
  transition: all 200ms ease-in-out 0s;
  box-shadow: 0 4px 10px -4px rgba(0, 0, 0, 0);
  border-color: rgba(0, 0, 0, 0.1);
}
.type {
  font-size: 1rem;
  background-color: #3eaf7c;
  display: inline;
  padding: 4px 8px;
  border-radius: 4px;
  color: white;
  text-transform: uppercase;
  font-size: 0.8rem;
}
</style>

