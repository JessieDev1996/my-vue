<template>
   <div>{{message}}</div>
    <PersonData name="แบงค์" salary=40000 />
    <PersonData name="โจโจ้" salary=20000 />
    <PersonData name="เจสซี้" salary=40000 />
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