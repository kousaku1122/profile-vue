<template>
  <v-navigation-drawer
    :value="value"
    app
    temporary
    clipped-right
    right
    @input="$emit('input', $event)"
  >
    <v-list nav dense>
      <nuxt-link v-scroll-to="'#about'" to>
        <v-list-item @click="drawerChange">
          <v-list-item-icon>
            <v-icon>mdi-account</v-icon>
          </v-list-item-icon>
          <v-list-item-title>About </v-list-item-title>
        </v-list-item>
      </nuxt-link>
      <nuxt-link v-scroll-to="'#skills'" to>
        <v-list-item @click="drawerChange">
          <v-list-item-icon>
            <v-icon>fas fa-code</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Skills</v-list-item-title>
        </v-list-item>
      </nuxt-link>
      <nuxt-link v-scroll-to="'#works'" to>
        <v-list-item @click="drawerChange">
          <v-list-item-icon>
            <v-icon>fas fa-paint-brush</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Works</v-list-item-title>
        </v-list-item>
      </nuxt-link>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  props: {
    value: false
  },

  methods: {
    drawerChange() {
      this.$emit("drawer", false);
    }
  }
};
</script>
