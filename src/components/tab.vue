<template>
  <div class="contain">
    <div class="tab" 
    v-for="(item,index) in tabs" 
    :key="index" 
    @click="current=index"
    :class="{'active':index==current}">
      {{item}}
    </div>
  </div>
</template>

<script>
export default {
  props:{
    tabs:{
      type:Object,
      default:()=>{
        return ['tab1','tab2']
      }
    }
  },
  data(){
    return{
      current:0
    }
    
  }
}
</script>

<style>
.contain {
  width: auto;
  height: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  background: burlywood;
  border-radius: 8px;
}
.tab {
  font-size: 20px;
  border-radius: 8px;
  width: 50%;
  padding: 10px;
}
.active{
  background: #f40;
  color: #fff;
}
</style>