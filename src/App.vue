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

  <!-- conditional rendering -->
  <button @click="status = !status">toggle</button>
    <div v-if="status">kondisi benar</div>
    <div v-else>kondisi salah</div>
    <div v-if="grade === 'A'">A</div>
    <div v-else-if="grade === 'B'">B</div>
    <div v-else-if="grade === 'C'">C</div>
    <div v-else>Not A/B/C</div>

  <!-- list rendering -->
  <ol>
    <li v-for="todo in todos" :key="todo.id">{{ todo.nama }}</li>
    <li v-for="(todo, index) in todos" :key="todo.id">index ke - {{ index }} {{ todo.nama }}</li>
  </ol>
</template>
<script>
export default {
  data() {
    return {
      message : "hello word",
      count : 0,
      pesan : "hello",
      status : true,
      grade: "B",
      todos : [
        {id : 1, nama: "dodi"},
        {id : 2, nama: "toni"},
        {id : 3, nama: "dodo"},
      ]
    }
  },
  methods : {
    minusCount () {
      this.count -= 1
    }
  }
}
</script>