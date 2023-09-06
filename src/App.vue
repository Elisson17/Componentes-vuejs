<template >
  <v-app >
    <v-main>
   <AuroraHeader />
   <AuroraContatos />
   <AuroraChat />
    </v-main>
  </v-app>
</template>

<script>
import AuroraHeader from './components/AuroraHeader.vue';
import AuroraContatos from './components/AuroraContatos.vue';
import AuroraChat from './components/AuroraChat.vue';
export default {
  name: 'App',

  components: {
    AuroraHeader,AuroraContatos,AuroraChat
  },

  data: () => ({
    //
  }),
}
</script>
