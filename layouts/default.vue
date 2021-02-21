<template lang="pug">
  .container.is-fullhd
    nav.navbar.nav-header(role="navigation" aria-label="Main navigation")
      .navbar-brand
        a.navbar-item(href='/')
          b Daniel Cañada
      .navbar-end
        .navbar-item
          .icon
            i.fab.fa-github
        .navbar-item
          .icon
            i.fab.fa-twitter

    .columns
      .column
        Nuxt
      aside.column.is-2.p-4
        .field
          .control.has-icons-left
            input.input.is-small(placeholder="Search posts")
            .icon.is-left
              i.fas.fa-search
        .card
          .card-content
            .title.is-6 Categories
            ul
              li
                nuxt-link(to="/")
                  b Index
              li
                nuxt-link(to="/about")
                  b About
              li
                nuxt-link(to="/inspire")
                  b Inpire

</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        },
        {
          title: 'About me',
          icon: 'account',
          to: { name: 'about' }
        }
      ]
    }
  }
}
</script>
<style>
html {
  background-color: #f9f9f9;
}
nav.nav-header {
  position: sticky;
  top: 0;
  border: 1px solid #e0e0e0;
  box-shadow: 0 0 4px rgba(0,0,0,0.2);
  margin-bottom: 1rem;
}
</style>
