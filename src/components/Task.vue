<template>
  <div class="box has-text-weight-bold">
    <div class="columns">
      <div class="column is-7">
        Descricao da Tarefa
      </div>
      <div class="column">
        <StopWatch :count="15" />
      </div>
    </div>


  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import StopWatch from './StopWatch.vue';

export default defineComponent({
  name: 'Task',

  components: {
    StopWatch
  }
})
</script>

<style scoped>
.box {
  background: #faf0ca;
}
</style>