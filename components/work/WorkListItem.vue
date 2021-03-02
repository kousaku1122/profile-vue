<template>
  <v-tabs-items :value="value" @change="$emit('change', value)">
    <div v-for="(tab, i) in tabs" :key="i">
      <v-tab-item :value="`${tab.value}`" eager>
        <v-card flat>
          <v-btn
            rounded
            :href="`${tab.url}`"
            min-width="100%"
            style="text-transform: none"
            class="mt-3 mb-2 text-caption"
          >
            <v-icon v-text="icon" />
            {{ tab.url }}
          </v-btn>

          <v-container
            id="scroll-target"
            style="max-height: 500px"
            class="overflow-y-auto"
          >
            <v-container>
              <v-img :src="`${tab.img}`" eager></v-img>
            </v-container>
          </v-container>

          <div class="text-body-2 pl-8 py-5" v-html="`${tab.sentence}`"></div>
        </v-card>
      </v-tab-item>
    </div>
  </v-tabs-items>
</template>

<script>
export default {
  props: ["value"],
  data() {
    return {
      icon: "mdi-lock",
      tabs: [
        {
          value: "tab-1",
          url: "https://www.teamauelu.me/",
          img: require("@/assets/image/aueluweb.png"),
          sentence:
            "大阪府社会人フットサルチームのWebページになります．<br />大阪府社会人フットサルというキーワードでGoogle検索6位にヒット．友人との共同開発作品．<br />機能：選手、試合結果、練習予定表示機能、変更時のニュース追加機能、インスタグラム連動<br />開発言語：HTML、CSS、Ruby、Ruby on Rails、Javascript、Vue(Vuetify) <br />使用技術：Amazon S3、InstagramAPI"
        },
        {
          value: "tab-2",
          url: "https://aueluaccounting.herokuapp.com/",
          img: require("@/assets/image/aueluaccounting.png"),
          sentence:
            "個人情報が掲載されているため、BASIC認証を導入しています。</br>現在は会計引継ぎに伴い使用はしていません。</br>大阪府社会人フットサルチームの月会費管理アプリになります．<br />会計で直面した問題を解決すべく作成したアプリケーションです．<br />機能：背番号検索機能，支払い遅延色変更機能<br />開発言語：HTML、CSS、Ruby、Ruby on Rails、Javascript <br />使用技術：Rspec <br /> コードに関してはこちらからご確認いただけます。<a>https://github.com/kousaku1122/auelu_accounting</a>"
        },
        {
          value: "tab-3",
          url: "https://github.com/sofuetakuma112/tweet_list/tree/app/",
          img: require("@/assets/image/hack.png"),
          sentence:
            "2daysハッカソンの成果物になります。<br />デプロイしていないため、コードのみになります。<br />ツイートの保存リストを共有できるアプリケーション。<br />担当：フロントエンド<br />機能：ツイート検索、保存リスト作成、保存リスト共有<br />開発言語：HTML、CSS、Vue(Vuetify) 、node.js<br />使用技術：Firebase、TweetAPI"
        },
        {
          value: "tab-4",
          url: "https://exa-intern.glitch.me/",
          img: require("@/assets/image/exa-intern.png"),
          sentence:
            "5daysインターンでの成果物です。<br />機能：感想投稿機能、いいね機能<br />開発言語：HTML、CSS、Javascript <br />使用技術：Glitch"
        }
      ]
    };
  }
};
</script>
