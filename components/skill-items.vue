<template>
  <v-row justify="space-around">
    <v-col
      cols="6"
      md="3"
      class="text-center"
      v-for="skill in skills"
      :key="skill.img"
    >
      <v-hover v-slot="{ hover }">
        <v-card :elevation="hover ? 12 : 2">
          <v-img :src="`${skill.img}`" @click.stop="onClick(skill)"></v-img>
          <v-divider></v-divider>
          <p>{{ skill.name }}</p>
        </v-card>
      </v-hover>
    </v-col>
    <v-dialog width="500" v-model="dialog" v-if="currentName">
      <v-card>
        <v-toolbar color="primary" dark>{{ currentName.name }}</v-toolbar>
        <v-card-text>
          <v-list-item
            two-line
            v-for="about in currentName.abouts"
            :key="about.name"
          >
            <v-list-item-content>
              <v-list-item-title>{{ about.date }}</v-list-item-title>
              <v-list-item-subtitle class="wrap-text">
                {{ about.content }}
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-card-text>
        <v-card-actions class="justify-end">
          <v-btn @click="dialog = false">Close</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      currentName: null,
      skills: [
        {
          img: require("@/assets/image/html.png"),
          name: "HTML5",
          abouts: [
            {
              date: "2019.01",
              content: "独学で学習開始"
            },
            {
              date: "2020.08",
              content: "社会人フットサルチームのWebページ作成"
            },
            {
              date: "2020.09",
              content: "インターンシップでアプリケーション作成"
            },
            {
              date: "2020.10",
              content: "社会人フットサルチームの月会費アプリケーション作成"
            },
            {
              date: "2020.12",
              content: "講義で映画レビューページ作成"
            },
            {
              content: "その他学習でページ作成"
            }
          ]
        },
        {
          img: require("@/assets/image/css.png"),
          name: "CSS3",
          abouts: [
            {
              date: "2019.01",
              content: "独学で学習開始"
            },
            {
              date: "2020.08",
              content:
                "社会人フットサルチームのWebページ作成,フレームワーク（bootstrap）"
            },
            {
              date: "2020.09",
              content: "インターンシップでアプリケーション作成"
            },
            {
              date: "2020.10",
              content:
                "社会人フットサルチームの月会費アプリケーション作成,フレームワーク（bootstrap）"
            },
            {
              date: "2020.12",
              content: "講義で映画レビューページ作成"
            },
            {
              content: "その他学習でページ作成"
            }
          ]
        },
        {
          img: require("@/assets/image/javascript.png"),
          name: "Javascript",
          abouts: [
            {
              date: "2020.08",
              content:
                "社会人フットサルチームのWebページ作成,ロード画面及びページ先頭に戻るボタン実装"
            },
            {
              date: "2020.09",
              content:
                "インターンシップで基礎及びインターンシップの感想を共有するアプリケーション作成"
            },
            {
              date: "2020.10",
              content:
                "社会人フットサルチームの月会費アプリケーション作成,ページ先頭に戻るボタンの実装"
            },
            {
              content: "その他学習でページ作成"
            }
          ]
        },
        {
          img: require("@/assets/image/vue.png"),
          name: "Vue",
          abouts: [
            {
              date: "2020.12",
              content: "独学で学習開始"
            },
            {
              date: "2020.01",
              content: "Portfolio作成"
            },
            {
              content: "その他学習でページ作成"
            }
          ]
        },
        {
          img: require("@/assets/image/ruby.png"),
          name: "Ruby",
          abouts: [
            {
              date: "2020.04",
              content: "独学で学習開始,フレームワーク(Rails)"
            },
            {
              date: "2020.08",
              content:
                "社会人フットサルチームのWebページ作成,フレームワーク(Rails)"
            },
            {
              date: "2020.10",
              content:
                "社会人フットサルチームの月会費アプリケーション作成,フレームワーク(Rails)"
            },
            {
              content: "その他学習でページ作成"
            }
          ]
        },
        {
          img: require("@/assets/image/c.png"),
          name: "C",
          abouts: [
            {
              date: "2018.04",
              content: "講義で学習開始"
            },
            {
              date: "2020.11",
              content: "競技プログラミングに触れる(C++)"
            }
          ]
        },
        {
          img: require("@/assets/image/java.png"),
          name: "Java",
          abouts: [
            {
              date: "2018.09",
              content: "講義で学習開始"
            },
            {
              date: "2020.09",
              content:
                "講義の実験で、商品一覧に検索機能や並べ替え機能を追加。使用技術（AmazonDynamoDB、AmazonS3、AWSIAM）"
            }
          ]
        },
        {
          img: require("@/assets/image/excel.png"),
          name: "Excel",
          abouts: [
            {
              date: "2021.01",
              content:
                "講義で映画データを検索、閲覧履歴からおすすめを検索するシステムを開発"
            }
          ]
        }
      ]
    };
  },
  methods: {
    onClick(name) {
      this.dialog = true;
      this.currentName = name;
      console.log(this.currentName);
    }
  }
};
</script>
