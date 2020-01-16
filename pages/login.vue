<template>
  <div>
    <div class="uneve-title">
      <h1>Olá! Bem vindo a Unimed Pleno.</h1>
      <h4>Gravida id posuere risus pellentesque et nec aliquam, et phasellus sed integer fermentum ultrices congue faucibus consequat integer non porta amet orci egestas mollis bibendum posuere at gravida</h4>
      <div class="uneve-spacer-48"></div>
    </div>
    <div class="uneve-form-login">
      <uneve-form-input
        type="email"
        name="uneve-email"
        id="uneve-email"
        label="E-mail"
      />
      <div class="uneve-spacer-24"></div>
      <uneve-form-input
        type="password"
        name="uneve-password"
        id="uneve-password"
        label="Senha"
      />
      <div class="uneve-spacer-48"></div>
      <uneve-form-submit />
    </div>
  </div>
</template>

<script>
  import UneveFormInput from '~/components/UneveFormInput.vue'
  import UneveFormSubmit from '~/components/UneveFormSubmit.vue'

  export default {
    name: "login",
    components: {
      UneveFormInput,
      UneveFormSubmit
    },
    head () {
      return {
        title: 'Uneve - Unimed Pleno',
      }
    },
  }
</script>

<style scoped lang="sass">
.uneve-spacer-48
  height: 48px

.uneve-spacer-24
  height: 24px

h1
  color: #303C40
  font-weight: 600
  font-size: 28px
  line-height: 42px
  padding-bottom: 8px

h4
  color: #859194
  font-weight: normal
  font-size: 14px
  line-height: 21px

*
  font-family: Poppins, serif
  font-style: normal
</style>
