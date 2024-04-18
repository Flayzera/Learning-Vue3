<template>
  <section>
    <strong>{{ elapsedTime }}</strong>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'StopWatch',

  props: {
    count: {
      type: Number,
      default: 0
    }
  },

  computed: {
    elapsedTime(): string {
      return new Date(this.count * 1000).toISOString().substring(11, 19)
    }
  },
})
</script>

<style scoped></style>