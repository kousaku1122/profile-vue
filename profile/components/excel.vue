<template>
  <v-col cols="6" md="3" class="text-center">
    <v-hover v-slot="{ hover }">
      <v-card :elevation="hover ? 12 : 2">
        <v-dialog width="500">
          <template v-slot:activator="{ on, attrs }">
            <v-img :src="excel_image_src" v-bind="attrs" v-on="on"></v-img>
          </template>
          <template v-slot:default="dialog">
            <v-card>
              <v-toolbar color="primary" dark>ExcelVBA</v-toolbar>
              <v-card-text>
                <v-list-item two-line>
                  <v-list-item-content>
                    <v-list-item-title>2021.01</v-list-item-title>
                    <v-list-item-subtitle class="wrap-text">
                      講義で映画データを検索、閲覧履歴からおすすめを検索するシステムを開発
                    </v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn text @click="dialog.value = false">Close</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
        <v-divider></v-divider>
        <p>ExcelVBA</p>
      </v-card>
    </v-hover>
  </v-col>
</template>

<script>
export default {
  data() {
    return {
      excel_image_src: require("@/assets/image/excel.png")
    };
  }
};
</script>
