<template>
<v-app>
  <v-app-bar  dark fixed app>
    <v-toolbar-title>Nuxt Jwt Auth</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text to="/profile">プロフィール</v-btn>
      <v-btn text>ログアウト</v-btn>
      <v-btn text to="/login">ログイン</v-btn>
    </v-toolbar-items>
  </v-app-bar>
  <v-main>
    <v-container fluid fill-height>
      <nuxt/>
    </v-container>
  </v-main>
</v-app>
</template>

<style>
</style>
