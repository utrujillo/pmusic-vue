<template lang="pug">
  li.artist 
    h2: a(v-bind:href="artist.url" target="_blank") {{ artist.name }}
    img(v-bind:src="artist.image[2]['#text']")
</template>

<script>
export default {
  name: 'artist', //este nombre tiene que coincidir con el nombre con el que se llama desde App.vue
  props: [
    'artist', // Es la propiedad que se pasa utilizando el v-bind
  ]
}
</script>

<style lang="stylus" scoped>
  li.artist
    display block
    margin 0 10px
</style>
