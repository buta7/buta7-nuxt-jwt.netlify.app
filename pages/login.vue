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
        v-model="name"
        label="ユーザID"
        required
      />
      <v-text-field
        v-model="password"
        label="パスワード"
        required
      />
    </v-card-text>

    <v-btn dark>ログイン</v-btn>
  </v-card>
</v-form>
</v-container>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      password: '',
      error: false
    }
  },
}
</script>

<style>
</style>
