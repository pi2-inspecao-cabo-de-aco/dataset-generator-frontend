<template lang="pug">
  q-page.index.column.flex-center.bg-secondary
    q-uploader(
      url="http://localhost:5000/upload"
      label="Carregue arquivos para gerar o Dataset"
      color="primary"
      multiple
    ).no-shadow

    q-select(
      standout
      v-model="model"
      :options="options"
      label="Rótulo para as imagens carregadas"
      options-dense
      stack-label
      bg-color="primary"
      color="white"
      dark
    ).q-mt-lg

    q-btn(
      color="accent"
      no-caps
      unelevated
    ).q-mt-lg Gerar CSV
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      model: null,
      options: [
        'Google', 'Facebook', 'Twitter', 'Apple', 'Oracle'
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~quasar-variables'
.index
  .q-uploader
    min-width 500px
    min-height 200px
    background $secondary

  .q-select
    min-width 500px
</style>

<style lang="stylus">
@import '~quasar-variables'
.index
  .q-uploader__list
    background #1c2633

  .q-field--dark.q-field--focused
    .q-field__native
      color white !important
</style>
