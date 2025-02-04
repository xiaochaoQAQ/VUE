<script setup>
import store from '@/store'
import {
  HomeFilled
} from '@element-plus/icons-vue'

const menuList = JSON.parse(sessionStorage.getItem("menuList"))

const openTab = (item) => {
  store.commit('ADD_TABS', item)
}

</script>

<template>
  <el-menu
      active-text-color="#FF4500"
      background-color="#00CED1"
      router
      class="el-menu-vertical-demo"
      text-color="#222222"
      :default-active="'/index'"
  >
    <el-menu-item index="/index" @click="openTab({name:'首页',path:'/index'})">
      <el-icon>
        <home-filled/>
      </el-icon>
      <span>首页</span>
    </el-menu-item>

    <el-sub-menu :index="menu.path" v-for="menu in menuList">
      <template #title>
        <el-icon>
          <svg-icon :icon="menu.icon"/>
        </el-icon>
        {{ menu.name }}
      </template>
      <el-menu-item :index="item.path" v-for="item in menu.children" @click="openTab(item)">
        <el-icon>
          <svg-icon :icon="item.icon"/>
        </el-icon>
        {{ item.name }}
      </el-menu-item>
    </el-sub-menu>
  </el-menu>

</template>

<style scoped>

</style>