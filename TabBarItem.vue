<template>
      <div class="tabbar-item" @click="ItemClick">
          <div v-if="!isActive"><slot name="item-icon"></slot></div>
          <div v-else ><slot name="item-icon-active"></slot></div>
          <div :class="{active : isActive}">
          <slot name="item-text"></slot>
          </div>
      </div>
</template>

<script>
export default {
    name : 'TabBarItem',
    props:{
        path: String
    },
    data() {
        return {
            // isActive : false
        }
    },
    computed: {
        isActive(){
            return this.$route.path.indexOf(this.path) !=-1
        }
    },
    methods: {
        ItemClick(){
            this.$router.replace(this.path).catch(err=>err)
        }
    },
}
</script>

<style>
.tabbar-item {
  flex: 1;
  font-size: 14px;
  text-align: center;
  height: 49px;
}
.tabbar-item img{
    width: 22px;
    vertical-align: middle;
   margin: 2px 0;
}

.active{
    color:#d4237a ;
}
</style>