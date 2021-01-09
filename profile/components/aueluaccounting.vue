<template>
  <v-img
  :src="image_src"
  v-bind="attrs"
  v-on="on"
  ></v-img>
</template>

<script>
  export default {
    data () {
      return {
        image_src: require("@/assets/image/aueluaccounting.png"),
      }
  }
}
</script>
