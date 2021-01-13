<template>
  <v-container fluid id="about">
    <v-row justify="space-around">
      <v-col cols="11" md="6">
        <v-card class="text-center">
          <div class="title pb-2">About</div>
          <v-divider inset dark></v-divider>
          <v-avatar size="250" class="my-10">
            <v-img :src="image_src"></v-img>
          </v-avatar>
          <div class="title mb-1">Koki Sakurai</div>
          <p>22年卒同志社大学理工学部インテリジェント情報工学科所属</p>
          <p>フットサル、サッカー、ツーリング、多趣味なエンジニア</p>
        </v-card>
      </v-col>

      <v-col cols="11" md="5">
        <v-card>
          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2018.04</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-cuttlefish</v-icon>
                c#を講義で学習、プログラミングに興味を持つようになる</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2018.09</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-java</v-icon>
                Javaを講義で学習</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.01</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-html5</v-icon>
                <v-icon>fab fa-css3-alt</v-icon>
                HTML、CSSを独学で習得</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.04</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fas fa-gem</v-icon>
                Ruby、Ruby on Railsを独学で習得</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.08</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fas fa-gem</v-icon>
                RubyでチームのWebページ作成、Bootstrapを習得</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.09</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-js</v-icon>
                Javascriptをインターンで習得</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.10</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fas fa-gem</v-icon>
                Rubyでチームの月会費管理アプリ作成</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.12~</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-vuejs</v-icon>Vueを学習中</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.12~</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-vuejs</v-icon> Joicul参加中</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.01</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fab fa-vuejs</v-icon>
                ハッカソン参加予定</v-list-item-subtitle
              >
            </v-list-item-content>
          </v-list-item>

          <v-list-item two-line>
            <v-list-item-content>
              <v-list-item-title>2020.01</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                <v-icon>fas fa-file-excel</v-icon>
                ExcelVBA講義で学習</v-list-item-subtitle
              >
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
      image_src: require("@/assets/image/logo.png")
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
