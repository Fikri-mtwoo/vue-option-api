<template>
    <div id="pesan">{{ message }}</div>

    <button @click="message='hello vue'">rubah</button>
</template>
<script>
    export default {
        props : {
            title : {
                type: String,
                default: ""
            }
        },
        data() {
            return {
                message : "hello word"
            }
        },
        beforeCreate () {
            console.log('before create')
            console.log(this.message)
        }, 
        created () {
            //bisa membaca semua variable setelah di render
            console.log('created')
            console.log(this.message)
        },
        beforeMount() {
            console.log('before mount')
            console.log(this.message)
            console.log(document.querySelector('#pesan'))
        },
        mounted() {
            //bisa membaca semua tag setelah di render
            console.log('mounted')
            console.log(this.message)
            console.log(document.querySelector('#pesan'))
        },
        beforeUpdate(){
            console.log('before updated')
            console.log(document.querySelector('#pesan').textContent)
        },
        updated(){
            //membaca semua perubahan data setelah di render
            console.log('updated')
            console.log(document.querySelector('#pesan').textContent)
        },
        beforeUnmount(){
            console.log('before unmount')
        },
        unmounted(){
            console.log('unmount')
        }
    }
</script>