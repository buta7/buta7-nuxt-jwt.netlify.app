# nuxt-jwt-example

Netlifyに外部認証で制限できることを確認(2020/08/31)

## Build Setup

```shell
npx create-nuxt-app nuxt-jwt-example
npm run dev
```

```shell
npm install --save @nuxtjs/axios @nuxtjs/auth @nuxtjs/vuetify
npm install --save dotenv
```

## Mock API server

```
cd express-jwt-mock
make
サーバを起動しました。http://localhost:8080
```

## Deploy to Netlify

* Build settings
    * Repository: github
    * Build command: npm run generate
    * Publish directory: dist 
* 環境変数
    * `AUTH_API_ENDPOINT`

## Link

* axios
    * [Options \- Axios Module](https://axios.nuxtjs.org/options/)
* cors
    * [【Nuxt\.js/axios】別ドメインへのajaxがCORS policyで弾かれる問題の対応 \- フリーランチ食べたい](https://blog.ikedaosushi.com/entry/2019/02/09/013404)
* auth
    * [NuxtでJWT認証を導入する \| WINDIIテック](https://tech.windii.jp/frontend/nuxt/nuxt-jwt-tutorial)
    * [猿でも分かる\!\! Nuxt\.jsのauthモジュール \- Qiita](https://qiita.com/kj455/items/66a1aab1524af51160ff)
    * [Auth Module \| Auth Module](https://auth.nuxtjs.org/)
    * [Nuxt\.jsのauth moduleとrails APIモードを使用したJWT認証の実装方法について②](https://www.for-engineer.life/entry/nuxt-rails-jwt2/)
    * [nuxt\-jwt\-example/login\.vue at master · windii\-legend/nuxt\-jwt\-example](https://github.com/windii-legend/nuxt-jwt-example/blob/master/pages/login.vue)
* netlify
    * [Nuxt\.jsでNetlifyにデプロイする時にパスのリライト設定をする \- Qiita](https://qiita.com/kaki_0704/items/8174b0e6eed7a7f762dc)
    * [Rewrites and proxies \| Netlify Docs](https://docs.netlify.com/routing/redirects/rewrites-proxies/#signed-proxy-redirects)
* backend
    * [GitHub \- windii\-legend/express\-jwt\-mock: Express（Node\.js\)のJWTモックサーバー](https://github.com/windii-legend/express-jwt-mock)
* error/warning
    * [LinuxでSystem limit for number of file watchers reachedが出る原因と対策](https://www.virment.com/how-to-fix-system-limit-for-number-of-file-watchers-reached/)
    * [javascript \- DevTools failed to load SourceMap: Could not load content for chrome\-extension \- Stack Overflow](https://stackoverflow.com/questions/61339968/devtools-failed-to-load-sourcemap-could-not-load-content-for-chrome-extension)
