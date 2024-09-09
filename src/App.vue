<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app>
      <v-list-item title="Vue.js" subtitle="Lista de Tarefas"></v-list-item>
      <v-divider></v-divider>
      <v-list>
        <v-list-item
          v-for="(item, index) in itens"
          :key="index"
          :to="item.to"
          link
          class="d-flex align-center"
        >
          <v-icon left>{{ item.icon }}</v-icon>
          <span class="ml-3">{{ item.title }}</span>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      prominent
      color="teal darken-4"
    >
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>Application</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      itens: [
        { title: "Tarefas", icon: "mdi-view-dashboard", to: '/' },
        { title: "Sobre", icon: "mdi-help-box", to: '/sobre' },
      ],
    };
  },
};
</script>

<style scoped>
/* Estilizações adicionais se necessário */
</style>
