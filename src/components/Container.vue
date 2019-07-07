<template>
  <div class="app">
    <el-container>
      <el-header class="app-header">
          <div class="app-header-logo">Vue-Admin</div>
          <div class="app-header-top">
            <div class="app-header-left">
              <div class="app-header-item"><i class="el-icon-s-fold"></i></div>
              <div class="app-header-item"><i class="el-icon-refresh"></i></div>
            </div>
            <div class="app-header-right">
              <div class="app-header-item"><i class="el-icon-chat-dot-round"></i></div>
              <div class="app-header-item">
                <el-dropdown trigger="click">
                  <span class="el-dropdown-link">
                    {{ username }}<i class="el-icon-arrow-down el-icon--right"></i>
                  </span>
                  <el-dropdown-menu slot="dropdown">
                    <el-dropdown-item>修改密码</el-dropdown-item>
                    <el-dropdown-item divided >退出登录</el-dropdown-item>
                  </el-dropdown-menu>
                </el-dropdown>
              </div>
            </div>
          </div>
        </el-header>
        <el-container>
          <el-aside class="app-side">
            <!-- 我是样例菜单 -->
            <el-menu class="el-menu-vertical-demo app-side-ul" >
              <el-submenu index="1">
                <template slot="title">
                  <i class="el-icon-location"></i>
                  <span slot="title">导航一</span>
                </template>
                <el-menu-item-group>
                  <el-menu-item index="1-1">选项1</el-menu-item>
                  <el-menu-item index="1-2">选项2</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <span slot="title">选项4</span>
                  <el-menu-item index="1-4-1">选项1</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-menu-item index="2">
                <i class="el-icon-menu"></i>
                <span slot="title">导航二</span>
              </el-menu-item>
              <el-menu-item index="4">
                <i class="el-icon-setting"></i>
                <span slot="title">导航四</span>
              </el-menu-item>
            </el-menu>
        </el-aside>
        <el-main class="app-body">
          <template>
            <router-view/>
          </template>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'Container',
  data () {
    return {
      username: 'Vue-Admin'
    }
  }
}
</script>
<style>
</style>
