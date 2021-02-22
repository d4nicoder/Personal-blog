<template lang="pug">
  div
    .background
    .login-container
      .card(style="margin-top: 3rem;")
        .card-content
          form(method="post" @submit.prevent="login()")
            .has-text-centered.mb-3
              img(src="/hacker.svg" style="width:80px")
              .title.is-4 Login
            .field
              .control.has-icons-left
                input.input.is-small(type="text" v-model="username" placeholder="Username" aria-label="User name")
                .icon.is-left
                  i.fas.fa-user

            .field
              .control.has-icons-left
                input.input.is-small(type="password" v-model="password" placeholder="Password" aria-label="Password")
                .icon.is-left
                  i.fas.fa-lock

            .has-text-centered
              button.button.is-primary.is-small.is-fullwidth(
                type="submit"
              )
                span Login
</template>
<script>
export default {
  layout: 'admin',
  data () {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    login () {
      console.log('Login')
    }
  }
}
</script>
<style lang="sass" scoped>
.login-container
  display: flex
  height: 100%
  flex-direction: column
  justify-content: center
  align-content: center
  align-items: center
  align-self: center

.background
  position: absolute
  display: block
  filter: blur(0.5rem)
  background-image: url(https://images.unsplash.com/photo-1498050108023-c5249f4df085?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1952&q=800)
  background-size: cover
  background-align: center
  background-repeat: no-repeat
  top: 0
  left: 0
  right: 0
  bottom: 0
</style>
