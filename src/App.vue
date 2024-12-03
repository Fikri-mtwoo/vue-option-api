<template>
  <!-- deklarative rendering -->
   <div>{{ message }}</div>
   <span :title="message">saya sedang belajar vue 3</span>

   <!-- methods -->
    <div>{{ count }}</div>
    <button @click="count++">tambah</button>
    <button @click="minusCount()">kurang</button>
</template>
<script>
export default {
  data() {
    return {
      message : "hello word",
      count : 0
    }
  },
  methods : {
    minusCount () {
      this.count -= 1
    }
  }
}
</script>