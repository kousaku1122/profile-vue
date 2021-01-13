<template>
  <v-container fluid id="works">
    <v-card>
      <div class="title pb-2 text-center">Works</div>
      <v-divider inset dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">
        リンクをクリックすることでページに飛びます
      </div>
      <v-tabs fixed-tabs v-model="tab">
        <v-tab href="#tab-1"> AueluWeb </v-tab>
        <v-tab href="#tab-2"> AueluAccounting</v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <v-tab-item value="tab-1" eager>
          <v-card flat>
            <v-btn
              rounded
              href="https://www.teamauelu.me/"
              min-width="100%"
              style="text-transform: none"
              class="mt-3 mb-2"
            >
              <v-icon style="text-align: right;">mdi-lock</v-icon>
              https://www.teamauelu.me/
            </v-btn>
            <v-container
              id="scroll-target"
              style="max-height: 500px"
              class="overflow-y-auto"
            >
              <AueluWeb />
            </v-container>
            <div class="text-body-1 pl-8 py-5">
              大阪府社会人フットサルチームのWebページになります．<br />大阪府社会人フットサルというキーワードでGoogle検索8位でヒット．友人との共同開発作品．<br />機能：選手，試合結果，練習予定表示機能，変更時のニュース追加機能<br />開発言語：HTML、CSS、Ruby、Ruby
              on Rails、Javascript <br />使用技術：Amazon S3
            </div>
          </v-card>
        </v-tab-item>
        <v-tab-item value="tab-2" eager>
          <v-card flat>
            <v-btn
              rounded
              href="https://aueluaccounting.herokuapp.com/"
              min-width="100%"
              style="text-transform: none"
              class="mt-3 mb-2"
            >
              <v-icon style="text-align: right;">mdi-lock</v-icon>
              https://aueluaccounting.herokuapp.com/
            </v-btn>
            <v-container
              id="scroll-target"
              style="max-height: 500px"
              class="overflow-y-auto"
            >
              <AueluAccounting />
            </v-container>
            <div class="text-body-1 pl-8 py-5">
              大阪府社会人フットサルチームの月会費管理アプリになります．<br />会計で直面した問題を解決すべく作成したアプリケーションです．<br />機能：背番号検索機能，支払い遅延色変更機能<br />開発言語：HTML、CSS、Ruby、Ruby
              on Rails、Javascript <br />使用技術：Rspec
            </div>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </v-container>
</template>

<script>
import AueluWeb from "@/components/aueluweb.vue";
import AueluAccounting from "@/components/aueluaccounting.vue";
export default {
  data() {
    return {
      tab: "tab-1"
    };
  },
  components: {
    AueluWeb,
    AueluAccounting
  }
};
</script>
