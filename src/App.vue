<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
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

    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>Application</v-app-bar-title>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    itens: [
      { title: "Tarefas", icon: "mdi-view-dashboard", to: '/'  },
      { title: "sobre", icon: "mdi-help-box", to: '/sobre'  },
    ],
  }),
}
</script>
