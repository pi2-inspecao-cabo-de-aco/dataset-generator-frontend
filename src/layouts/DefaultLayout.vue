<template lang="pug">
  q-layout(view="hHh lpR lFf")

    q-header(reveal).bg-primary.text-white
      q-toolbar
        q-btn(dense flat round icon="menu" @click="left = !left").no-shadow.cursr-pointer

        q-toolbar-title
          q-icon(name="mdi-database-plus").q-mr-sm
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
