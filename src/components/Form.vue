<template>
  <div class="box">
    <div class="columns">
      <div class="column is-8" role="form" aria-label="Formulário para criacao de uma nova tarefa">
        <input type="text" class="input" placeholder="Qual  tarefa voce deseja iniciar">
      </div>
      <div class="column">
        <Timer />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import Timer from './Timer.vue';

export default defineComponent({
  name: 'Form',

  components: {
    Timer
  }

})
</script>