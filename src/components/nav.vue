<template>
  <div class="contain">
    <div class="fanhui" v-text="'<'"></div>
    <div v-show="obj.mid">
      {{obj.title}}
    </div>
    <slot name="mid"></slot>
    <div v-show="obj.right">
      ...
    </div>
    <slot name="right"></slot>
  </div>
</template>

<script>
export default {
props:{
  obj:{
    type:Object,
    default:()=>{
      return{
        title:'默认标题',
        mid:true,
        right:true
      }
    }
  }
}
}
</script>

<style scope>
.contain{
  width: 500px;
  height: 60px;
  display:flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}
</style>