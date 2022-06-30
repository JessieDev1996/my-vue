<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <img v-bind:src="picture" v-bind:width="size" v-bind:height="size" ref="imageURL"/>
  <img :src="picture" :width="size" :height="size"/><br/>
  <form v-on:submit="submitform">
  ป้อนชื่อเล่น : <input type="text" v-on:input="setNickName" ref="nickNameEL"/>
  <button type="submit">บันทึก</button>
    </form>
  <h1>ชื่อนามสกุล :{{getFullname()}}</h1>
  <h1>ชื่อผู้สมัครงาน :{{firstname}}</h1>
  <h1>ชื่อเล่น :{{nickname}}</h1>
  <h1>นามสกุล :{{lastname}}</h1>
  <h1>อายุ :{{age}}</h1>
  <h1>{{100+200}}</h1>
  <p>ที่อยู่ : <span v-html="address"></span></p>
  <a :href="social" target="_blank">facebook</a>
  <p>งานอดิเรก :{{hobby[0]}},{{hobby[1]}},{{hobby[2]}}</p>
  <p>เพศ :{{general.gender}}</p>
  <p>น้ำหนัก :{{general.gender}} kg.</p>
  <p>เพศ :{{general.height}} cm.</p>
  <p>โรคประจำตัว : {{general.status}}</p>
  <button v-on:click="showData">คลิกเพื่อดูข้อมูล</button>
  <button @click="showData">คลิกเพื่อดูข้อมูล2</button>
  <button @click="increment">เพิ่ม</button>
  <button @click="decrement">ลด</button>
  <button @click.ctrl="incrementValue(10)">เพิ่ม 10</button>
  <button @click.middle="decrementValue(3)">ลด 3</button>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){ // รีเทิร์น ข้อมูล
    return{
      firstname:"แบงค์",
      lastname :"Jessie",
      nickname :"",
      age: 16,
      address:"<strong>กรุงเทพมหานคร</strong>",
      picture:"https://cdn-icons.flaticon.com/png/512/2171/premium/2171990.png?token=exp=1656591800~hmac=22e8501a2ff3c023e05e33caa1b73037",
      size: 50,
      social:"https://web.facebook.com/BankKts.96/",
      hobby:["Football","PlayGame","Music"],
      general:{gender:"male",weight:67,height:174,status:false}
    }
  },
  methods :{
    getFullname(){
      return this.firstname + this.lastname
    },
    showData(){
      alert(this.firstname)
    },
     increment(){

        this.age++
    },incrementValue(value){

        this.age = this.age + value
    },
      decrement(){
      this.age--
    },
      decrementValue(value){
      this.age = this.age - value
    },
    setNickName(event){
     this.nickname = event.target.value;
    },
    submitform(e)
    {
      e.preventDefault();
      alert("บันทึกชื่อเล่นให้หน่อย")
      console.log(this.$refs.imageURL);
      console.log(this.$refs.nickNameEL);
    }
  },
  // components: {
  //   HelloWorld
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
