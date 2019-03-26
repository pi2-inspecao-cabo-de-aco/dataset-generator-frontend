<template lang="pug">
  q-layout(view="hHh lpR lFf")

    q-header(reveal).bg-light-blue-10.text-white
      q-toolbar
        q-btn(dense flat round icon="menu" @click="left = !left").no-shadow

        q-toolbar-title
          span Dataset Generator

    q-drawer(v-model="left" side="left" bordered)

    q-page-container
      router-view
</template>

<script>
export default {
  data () {
    return {
      left: true
    }
  }
}
</script>

<script>

export default {
  name: 'MyLayout',
  data () {
    return {
      left: false
    }
  }
}
</script>

<style>
</style>
