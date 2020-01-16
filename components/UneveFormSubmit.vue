<template>
    <div>
      <button type="submit">Começar cadastro</button>
    </div>
</template>

<script>
    export default {
        name: "UneveFormSubmit"
    }
</script>

<style scoped lang="sass">
button
  padding: 15px 40px
  width: 273px
  height: 60px
  background: #01C0C8
  border-radius: 16px
  font-weight: 600
  font-size: 18px
  line-height: 30px
  text-align: center
  color: #FFFFFF
  border: none

@media (max-width: 768px)
  button
    width: 100%
</style>
