<template>
  <v-app>
          <v-navigation-drawer
        v-model="drawer"
        :rail="rail"
        permanent
        @click="rail = false"
        color="#0C1B33"
      >
        <v-list-item
          style="color: #D9BBF9; font-size:1.4em"
          prepend-icon="mdi-account-box"
          title="Mihaly de Bie"
          nav
        >
          <template v-slot:append>
            <v-btn
              icon="mdi-chevron-left"
              variant="text"
              @click.stop="rail = !rail"
            ></v-btn>
          </template>
        </v-list-item>

        <v-divider></v-divider>

        <v-list density="compact" nav style="color: #DB5461">
          <v-list-item prepend-icon="mdi-home-city" title="Home" value="home" style="color: #EFF8E2" :to="{ path: '/' }"> </v-list-item>
          <v-list-item prepend-icon="mdi-account" title="Guidelines" value="account" style="color: #EFF8E2" :to="{ path: '/guidelines' }"></v-list-item>
          <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users" style="color: #EFF8E2"></v-list-item>
        </v-list>
      </v-navigation-drawer>
    
    
        <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
  export default {
    data () {
      return {
        drawer: true,
        rail: false,
      }
    },
  }
</script>


