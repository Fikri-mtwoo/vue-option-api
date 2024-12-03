<template>
  <!-- deklarative rendering -->
   <div>{{ message }}</div>
   <span :title="message">saya sedang belajar vue 3</span>

   <!-- methods -->
    <div>{{ count }}</div>
    <button @click="count++">tambah</button>
    <button @click="minusCount()">kurang</button>

  <!-- input binding -->
  <!-- 2 away binding -->
    <div>{{ pesan }}</div>
    <input 
      :value="pesan"
      @input="event => pesan = event.target.value">
  <!-- v-model -->
    <div>{{ pesan }}</div>
    <hr>
    <input type="text" v-model="pesan"><br>
</template>
<script>
export default {
  data() {
    return {
      message : "hello word",
      count : 0,
      pesan : "hello"
    }
  },
  methods : {
    minusCount () {
      this.count -= 1
    }
  }
}
</script>