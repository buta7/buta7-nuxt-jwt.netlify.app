<template>
<v-app>
  <v-app-bar  dark fixed app>
    <v-toolbar-title>Nuxt Jwt Auth</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
<v-btn text to="/profile" v-if="isAuthenticated">プロフィール</v-btn>
<v-btn text v-if="isAuthenticated" @click="logout">ログアウト</v-btn>
<v-btn text to="/login" v-if="!isAuthenticated">ログイン</v-btn>
    </v-toolbar-items>
  </v-app-bar>
  <v-main>
    <v-container fluid fill-height>
      <nuxt/>
    </v-container>
  </v-main>
</v-app>
</template>

<script>
export default {
computed: {
  isAuthenticated () {
    return this.$auth.loggedIn
  },
},
methods: {
  async logout() {
    await this.$auth.logout();
  },
}
}
</script>

<style>
</style>
