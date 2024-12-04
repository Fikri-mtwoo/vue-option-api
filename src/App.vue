<template>
  <h1>ini template parent</h1>
  <HeaderTemplate title="hello word" />
  <HeaderTemplate :title="message" />
  <hr>
  <BasicTemplate />
</template>

<script>
  import BasicTemplate from './components/BasicTemplate.vue';
  import HeaderTemplate from './components/HeaderTemplate.vue';
  export default {
    components : {
      BasicTemplate,
      HeaderTemplate
    },
    data() {
      return {
        message : "Title header"
      }
    }
  }
</script>