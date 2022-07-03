<template>
   <div>{{message}}</div>
    <PersonData />
</template>

<script>
import PersonData from './PersonData.vue'
export default {
    name:"ListData",
    data(){
        return{
            message:"ListData Component"
        }
    },
      components: {
    PersonData
  }
}
</script>

<style>

</style>