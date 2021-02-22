<template lang="pug">
.backoffice
  aside.side-menu
    .title.is-6 Menú
    ul
      li(v-for="item in menu")
        nuxt-link(:to="item.to") {{ item.name }}

  .backoffice-content
    NuxtChild
</template>
<script>
export default {
  layout: 'admin',
  data () {
    return {
      menu: [
        {
          name: 'Posts',
          icon: 'fas fa-edit',
          to: '/backoffice/posts'
        }
      ]
    }
  }
}
</script>
<style lang="sass" scoped>
aside.side-menu
  position: absolute
  left: 0
  top: 0
  bottom: 0
  width: 200px
  background-color: #eee

.backoffice-content
  position: absolute
  display: block
  left: 200px
  right: 0
  top: 0
</style>
