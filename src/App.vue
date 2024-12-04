<template>
  <h1>ini template parent</h1>
  <!-- <HeaderTemplate title="hello word" /> -->
  <!-- <HeaderTemplate :title="message" /> -->
   <!-- <HeaderTemplate v-for="buah in buahs" :key="buah" :title="buah"/> -->
  <!-- <hr> -->
  <!-- <BasicTemplate /> -->
   <!-- <BlankTemplate/> -->
    <ChildTemplate ref="childComponent" @child="onPessParent"/>
    <button @click="clickMe">parent button</button>
</template>

<script>
  import BasicTemplate from './components/BasicTemplate.vue';
  import HeaderTemplate from './components/HeaderTemplate.vue';
  import BlankTemplate from './components/BlankTemplate.vue';
  import ChildTemplate from './components/ChildTemplate.vue';
  export default {
    components : {
      BasicTemplate,
      HeaderTemplate,
      BlankTemplate,
      ChildTemplate
    },
    data() {
      return {
        message : "Title header",
        buahs : ["jeruk", "apel", "melon", "semangka"]
      }
    },
    methods : {
      onPessParent(val){
        console.log(`function dari parent ${val.nama}`)
      },
      clickMe(){
        this.$refs.childComponent.onClick()
      }
    }
  }
</script>