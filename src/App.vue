<template>
  <h1>ini template parent</h1>
  <!-- <HeaderTemplate title="hello word" /> -->
  <!-- <HeaderTemplate :title="message" /> -->
   <!-- <HeaderTemplate v-for="buah in buahs" :key="buah" :title="buah"/> -->
  <!-- <hr> -->
  <!-- <BasicTemplate /> -->
   <BlankTemplate/>
</template>

<script>
  import BasicTemplate from './components/BasicTemplate.vue';
  import HeaderTemplate from './components/HeaderTemplate.vue';
  import BlankTemplate from './components/BlankTemplate.vue';
  export default {
    components : {
      BasicTemplate,
      HeaderTemplate,
      BlankTemplate
    },
    data() {
      return {
        message : "Title header",
        buahs : ["jeruk", "apel", "melon", "semangka"]
      }
    }
  }
</script>