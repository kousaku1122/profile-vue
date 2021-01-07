<template>
  <v-col cols="6" md="3" class="text-center">
    <v-hover v-slot="{ hover }">
      <v-card  :elevation="hover ? 12 : 2">
        <v-dialog
        width="500"
        >
        <template v-slot:activator="{ on, attrs }">
          <v-img
          :src="javascript_image_src"
          v-bind="attrs"
          v-on="on"
          ></v-img>
        </template>
        <template v-slot:default="dialog">
          <v-card>
            <v-toolbar
            color="primary"
            dark
            >Javascript</v-toolbar>
            <v-card-text>
              <v-list-item two-line>
                <v-list-item-content>
                  <v-list-item-title>2020.08</v-list-item-title>
                  <v-list-item-subtitle class="wrap-text">
                    社会人フットサルチームのWebページ作成,ロード画面及びページ先頭に戻るボタン実装
                  </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>

              <v-list-item two-line>
                <v-list-item-content>
                  <v-list-item-title>2020.09</v-list-item-title>
                  <v-list-item-subtitle class="wrap-text">
                    インターンシップで基礎及びインターンシップの感想を共有するアプリケーション作成</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item two-line>
                  <v-list-item-content>
                    <v-list-item-title>2020.10</v-list-item-title>
                    <v-list-item-subtitle class="wrap-text">
                      社会人フットサルチームの月会費アプリケーション作成,ページ先頭に戻るボタンの実装
                    </v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item two-line>
                  <v-list-item-content>
                    <v-list-item-title></v-list-item-title>
                    <v-list-item-subtitle class="wrap-text">
                      その他学習でページ作成
                    </v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>

              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                text
                @click="dialog.value = false"
                >Close</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
        <v-divider></v-divider>
        <p>Javascript</p>
      </v-card>
    </v-hover>
  </div>
</v-col>
</template>

<script>
  export default {
    data () {
      return {
        javascript_image_src: require("@/assets/image/javascript.png"),
      }
  }
}
</script>
