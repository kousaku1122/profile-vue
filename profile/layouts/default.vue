<template>
  <v-app>
    <v-card
        class="mx-auto overflow-hidden"
        height="400"
        width="100%"
      >
      <Header @drawer="updateDrawer">
      </Header>
        <v-navigation-drawer
          v-model="drawer"
          app
          temporary
          clipped-right
          right
        >
          <v-list
            nav
            dense
          >
            <v-list-item-group
              v-model="group"
              active-class="deep-purple--text text--accent-4"
            >
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Home</v-list-item-title>
              </v-list-item>

              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-account</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Account</v-list-item-title>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-navigation-drawer>
        <v-card-text>
        <nuxt />
    </v-card-text>
      </v-card>

    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>


  </v-app>
</template>

<script>
import Header from '@/components/header.vue';
export default {
  data: () => ({
     drawer: false,
     group: null,
   }),
  components: {
    Header,
  },
  methods: {
      updateDrawer (value) {
        this.drawer = value
      }
    }
}
</script>
