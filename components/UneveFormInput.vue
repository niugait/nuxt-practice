<template>
  <div class="uneve-input">
    <label :for="name">{{ label }}</label>
    <input :type="type" :name="name" :id="id">
  </div>
</template>

<script>
  export default {
    name: "UneveFormInput",
    props: {
      name: {
        type: String,
        required: true
      },
      type: {
        type: String,
        required: true
      },
      id: {
        type: String,
        required: false
      },
      label: {
        type: String,
        required: false
      },
    }

  }
</script>

<style scoped lang="sass">
.uneve-input
  display: flex
  flex-direction: column

input
  border: 1.5px solid #859194
  box-sizing: border-box
  border-radius: 12px
  width: 50%
  height: 60px
  padding: 24px 20px

label
  color: #859194
  font-weight: 500
  font-size: 14px
  line-height: 21px
  margin-bottom: 8px

@media (max-width: 768px)
  input
    width: 100%
</style>
