<template>
  <div>
    我是首页
    <ul>
      <li @longtap="deleteOne(index)" v-for="(item, index) in list" :key="index">
        {{ item.name }}--- {{ item.study }}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    data:function(){
      return {
        list:[
          {name:"一颗牙疼",study:"考研加油"},
          {name:"添添宝贝猪",study:"Wait for you"},
        ]
      }
    },
    methods:{
      deleteOne(index){
        
        this.list.splice(index,1)
      }
    }
  }
</script>

<style>

</style>

