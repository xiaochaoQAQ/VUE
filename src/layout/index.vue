<script setup>
import Menu from "@/layout/menu"
import Footer from "@/layout/footer"
import Header from "@/layout/header"
import Tabs from "@/layout/tabs"
</script>

<template>
  <div class="app-wrapper">
    <el-container>
      <el-aside width="200px" class="sidebar-container">
        <Menu></Menu>
      </el-aside>
      <el-container>
        <el-header>
          <Header></Header>
        </el-header>
        <el-main>
          <Tabs></Tabs>
          <router-view/>
        </el-main>
        <el-footer>
          <Footer></Footer>
        </el-footer>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped>
.app-wrapper {
  position: relative;
  width: 100%;
  height: 100%;
}

.sidebar-container {
  background-color: #eee8e1;
  height: 100%;
}

.el-container {
  height: 100%;
  //background-color: #c6c6c4;
}

.el-header {
  padding-left: 0px;
  background-color: #8b7aa4;
  padding-right: 0px;
}

:deep(ul.el-menu) {
  border-right-width: 0px;

}

.el-footer {
  background-color: #dce29a;
}


</style>