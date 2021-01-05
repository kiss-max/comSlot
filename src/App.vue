<template>
  <div>
    <navv :obj="obj1"></navv>
    <navv :obj="obj2">
      <div slot="mid">
        <tabb></tabb>
      </div>
      <div slot="right">
        <img src="./assets/logo.png" class="rightimg">
      </div>
    </navv>
  </div>
  
</template>

<script>
import navv from './components/nav'
import tabb from './components/tab'
export default {
  components:{
    navv,tabb
  },
  data(){
    return{
      obj1:{
        title:'我是title1',
        mid:true,
        right:true
      },
      obj2:{
        title:'我是title2',
        mid:false,
        right:false
      },
    }
  }
}
</script>

<style>
.rightimg{
  width: 50px;
  height: 50px;
}
</style>
