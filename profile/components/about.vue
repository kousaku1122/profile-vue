<template>
  <v-container fluid>
    <v-row justify="space-around">
      <v-col cols="11" md="6">
        <v-card>
          <div class="title pb-2">About</div>
          <v-divider inset dark></v-divider>
          <v-img src="https://picsum.photos/510/300?random" aspect-ratio="1.7"
          rounded>
        </v-img>
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
            <v-list-item-subtitle>
              <fa :icon="faCuttlefish" /> c#を講義で学習、プログラミングに興味を持つようになる</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2018.09</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faJava" /> Javaを講義で学習</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.01</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faHtml5" />  <fa :icon="faCss3Alt" /> HTML、CSSを独学で習得</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.04</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faGem" /> Ruby、Ruby on Railsを独学で習得</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.08</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faGem" /> RubyでチームのWebページ作成、Bootstrapを習得</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.09</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faJs" /> Javascriptをインターンで習得</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.10</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faGem" /> Rubyでチームの月会費管理アプリ作成</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.12~</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faVuejs" /> Vueを学習中</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.12~</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faVuejs" /> Joicul参加中</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>2020.01</v-list-item-title>
            <v-list-item-subtitle>
              <fa :icon="faVuejs" /> ハッカソン参加予定</v-list-item-subtitle>
            </v-list-item-content>

          </v-list-item>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { faVuejs } from '@fortawesome/free-brands-svg-icons'
import { faHtml5 } from '@fortawesome/free-brands-svg-icons'
import { faCss3Alt } from '@fortawesome/free-brands-svg-icons'
import { faJava } from '@fortawesome/free-brands-svg-icons'
import { faJs } from '@fortawesome/free-brands-svg-icons'
import { faCuttlefish } from '@fortawesome/free-brands-svg-icons'
import { faGem } from '@fortawesome/free-solid-svg-icons'

export default {
  computed: {
    faVuejs () {
      return faVuejs
    },
    faHtml5 () {
      return faHtml5
    },
    faCss3Alt () {
      return faCss3Alt
    },
    faJava () {
      return faJava
    },
    faJs () {
      return faJs
    },
    faCuttlefish () {
      return faCuttlefish
    },
    faGem () {
      return faGem
    },
  },
}
</script>
