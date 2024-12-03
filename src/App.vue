<template>
  <!-- deklarative rendering -->
   <div>{{ message }}</div>
   <span :title="message">saya sedang belajar vue 3</span>
</template>
<script>
export default {
  data() {
    return {
      message : "hello word"
    }
  }
}
</script>