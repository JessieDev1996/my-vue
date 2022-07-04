<template>
  <h1>{{message}}</h1>
</template>

<script>
export default {
    name:"PersonData",
    data(){
        return{
            message:"ข้อมูลพนักงานของแต่ละคน"
        }
    }
}
</script>

<style scoped>
    h1{
        color: yellow;
    }
</style>

