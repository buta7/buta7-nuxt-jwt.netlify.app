<template>
<v-container>
<v-form>
  <v-card>
    <v-alert
      :value="error"
      type="error"
    >
      IDとパスワードの組みが正しくありません
    </v-alert>
    <v-card-title primary-title>
      <h3 class="headline mb-0">ログイン</h3>
    </v-card-title>
    <v-card-text>
      <v-text-field
        v-model="username"
        label="ユーザ名"
        prepend-icon="mdi-account-circle"

      />
      <v-text-field
        v-model="password"
        label="パスワード"
        prepend-icon="mdi-lock"
        :append-icon="show_password ? 'mdi-eye' : 'mdi-eye-off'"
        :type="show_password ? 'text' : 'password'"
        @click:append="show_password = !show_password"
      />
    </v-card-text>

    <v-btn dark @click="submit">ログイン</v-btn>
  </v-card>
</v-form>
</v-container>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
      error: false,
      show_password: false
    }
  },
  middleware: 'guest',
  methods: {
    async submit () {
      try {
        await this.$auth.loginWith('local', {
          data: {
            username: this.username,
            password: this.password,
            provider:  process.env.VUE_APP_AUTH_PROVIDER || 'local'
          }
        })
        this.$router.push('/profile')
      } catch (e) {
        this.error = true
      }
    }
  }
}
</script>

<style>
</style>
