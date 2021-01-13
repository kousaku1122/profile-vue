<template>
  <v-navigation-drawer
    :value="value"
    app
    temporary
    clipped-right
    right
    @input="$emit('input', $event)"
  >
    <v-list nav dense v-for="item in nav_items" :key="item.id">
      <nuxt-link v-scroll-to="`#${item.id}`" to>
        <v-list-item @click="drawerChange">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-title>{{ item.content }}</v-list-item-title>
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
  data() {
    return {
      nav_items: [
        { id: "about", icon: "mdi-account", content: "About" },
        { id: "skills", icon: "fas fa-code", content: "Skills" },
        { id: "works", icon: "fas fa-paint-brush", content: "Works" }
      ]
    };
  },

  methods: {
    drawerChange() {
      this.$emit("drawer", false);
    }
  }
};
</script>
