<template>
  <v-container fluid id="about">
    <v-row justify="space-around">
      <v-col cols="12" md="6">
        <v-card class="text-center">
          <div class="title pb-2">About</div>
          <v-divider dark></v-divider>
          <v-avatar size="250" class="my-10">
            <img src="~/assets/image/logo.png" />
          </v-avatar>
          <div class="title mb-1">Koki Sakurai</div>
          <p>22年卒同志社大学理工学部インテリジェント情報工学科所属</p>
          <p class="pb-8">
            フットサル、サッカー、ツーリング、多趣味なエンジニア
          </p>
        </v-card>
      </v-col>

      <v-col cols="12" md="5">
        <v-card>
          <v-list-item two-line v-for="about in abouts" :key="about.contents">
            <v-list-item-content>
              <v-list-item-title>{{ about.date }}</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>{{ about.icon }}</v-icon
                ><v-icon>{{ about.icon2 }}</v-icon>
                {{ about.contents }}
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      abouts: [
        {
          date: "2018.04",
          icon: "fab fa-cuttlefish",
          contents: "c#を講義で学習、プログラミングに興味を持つようになる"
        },
        {
          date: "2018.09",
          icon: "fab fa-java",
          contents: "Javaを講義で学習"
        },
        {
          date: "2020.01",
          icon: "fab fa-html5",
          icon2: "fab fa-css3-alt",
          contents: "HTML、CSSを独学で習得"
        },
        {
          date: "2020.04",
          icon: "fas fa-gem",
          contents: "Ruby、Ruby on Railsを独学で習得"
        },
        {
          date: "2020.08",
          icon: "fas fa-gem",
          contents: "RubyでチームのWebページ作成、Bootstrapを習得"
        },
        {
          date: "2020.09",
          icon: "fab fa-js",
          contents: "Javascriptをインターンで習得"
        },
        {
          date: "2020.10",
          icon: "fas fa-gem",
          contents: "Rubyでチームの月会費管理アプリ作成"
        },
        {
          date: "2020.12~",
          icon: "fab fa-vuejs",
          contents: "Vueを学習中"
        },
        {
          date: "2020.12~",
          icon: "fab fa-vuejs",
          contents: "Joicul参加中"
        },
        {
          date: "2020.01",
          icon: "fab fa-vuejs",
          contents: "ハッカソン参加予定"
        },
        {
          date: "2020.01",
          icon: "fas fa-file-excel",
          contents: "ExcelVBA講義で学習"
        }
      ]
    };
  }
};
</script>

<style>
.wrap-text {
  word-break: break-all;
  white-space: normal;
}
</style>
