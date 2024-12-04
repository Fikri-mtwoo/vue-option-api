<template>
    <div>total : {{ total }}</div>
    <div>perbandingan : {{ banding }}</div>
    <div>diskon : {{ discount }}</div>
    <input type="number" v-model="numb1">
    <input type="number" v-model="numb2">
    <button @click="diskon()">Diskon</button>
    <hr>
    <input v-model="message">
</template>
<script>
export default{
    data() {
        return {
            numb1 : 0,
            numb2 : 0,
            message : ""
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
        },
        discount : {
            get(){
                return this.numb1 + this.numb2
            },
            set(newVariable){
                this.numb1 -= newVariable
                this.numb2 -= newVariable
            }
        }
    },
    methods : {
        diskon(){
            this.discount = 500
        }
    },
    watch : {
        message(oldval, newVal){
            console.log(`${oldval} ${newVal}`)
        }
    }
}
</script>