<template>
    <div>ini component child</div>
    <button @click="onPress()">child button</button>
</template>
<script>
export default{
    data(){
        return {
            mhs : {
                nama:"abdul",
                jurusan:"Teknik Informatika"
            }
        }
    },
    emits : ['child'],
    methods : {
        onPress(){
            this.$emit('child', this.mhs)
        },
        onClick(){
            console.log('function dari child')
        }
    }
}
</script>