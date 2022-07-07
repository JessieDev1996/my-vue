<template>
  <h1>{{message}}</h1>
   <h1>{{name}}</h1>
   <h1>{{salary}}</h1>
</template>

<script>
export default {
    name:"PersonData",
    data(){
        return{
            message:"ข้อมูลพนักงานของแต่ละคน"
        }
    },
    props:["name","salary"]
}
</script>

<style scoped>
    h1{
        color: black;
    }
</style>

