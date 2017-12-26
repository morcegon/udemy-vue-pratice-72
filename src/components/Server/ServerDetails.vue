<template>
  <div class="col-xs-12 col-sm-6">
    <p v-if="!server">Please select a server</p>
    <template v-else>
      <p>Server #{{ server.id }} selected. Status: {{ server.status }}</p>
      <hr>
      <button
        v-if="server.status!=='Normal'"
        @click="resetStatus">Change Status</button>
    </template>    
  </div>
</template>

<script>
  import { serverBus } from '../../main';

  export default {
    data: () => {
      return {
        server: null
      }
    },
    methods: {
      resetStatus() {
        this.server.status = 'Normal'
      }
    },
    created() {
      serverBus.$on('serverSelected', (server) => {
        this.server = server;
      });
    }
  }
</script>
