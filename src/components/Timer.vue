<template>
  <div class="is-flex is-align-items-center is-justify-content-space-between">
    <StopWatch :count="count" />
    <button class="button" @click="start" :disabled="timerRunning">
      <span class="icon">
        <i class="fas fa-play"></i>
      </span>
      <span>play</span>
    </button>
    <button class="button" @click="stop" :disabled="!timerRunning">
      <span class="icon">
        <i class="fas fa-stop"></i>
      </span>
      <span>stop</span>
    </button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import StopWatch from './StopWatch.vue'

export default defineComponent({
  name: 'Timer ',

  components: {
    StopWatch
  },

  methods: {
    start() {
      this.timerRunning = true

      this.timer = setInterval(() => {
        this.count++
      }, 1000)
    },

    stop() {
      this.timerRunning = false

      clearInterval(this.timer)
    }
  },

  data() {
    return {
      count: 0,
      timer: 0,
      timerRunning: false
    }
  }

})
</script>