<template>
    <div>{{ total }}</div>
    <div>{{ banding }}</div>
    <input type="number" v-model="numb1">
    <input type="number" v-model="numb2">
</template>
<script>
export default{
    data() {
        return {
            numb1 : 0,
            numb2 : 0
        }
    },
    computed : {
        total() {
            return this.numb1 + this.numb2
        },
        banding() {
            if(this.numb1 > this.numb2){
                return "angka 1 lebih besar dari angka 2"
            }else{
                return "angka 2 lebih besar dari angka 1"
            }
        }
    }
}
</script>