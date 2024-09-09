<template>
  <div>
    <v-list lines="three" select-strategy="classic">
      <v-list-item value="notifications">
        <tarefa />

      </v-list-item>
    </v-list>
  </div>
</template>

<script lang="ts">
import tarefa from '../components/Tarefas/tarefa.vue';


export default {
  components: { tarefa },
  name: 'Home',

}

//
</script>
