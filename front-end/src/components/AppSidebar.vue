<template>
    <section class="app-sidebar">
        <div id="sidebarMenu" class="sidebar sidebar-offcanvas">
            <ul class="nav">
                <li class="nav-item nav-profile">
                    <div class="nav-link">
                        <div class="profile-name">
                            <p class="name">Superadmin</p>
                            <p class="designation">Admin</p>
                        </div>
                    </div>
                </li>
            </ul>
            <el-menu
                    default-active="2"
                    class="el-menu-vertical-demo">
                <el-menu-item index="1">
                    <i class="el-icon-menu"></i>
                    <span>Namecheap</span>
                </el-menu-item>
                <el-submenu index="2">
                    <template slot="title">
                        <i class="el-icon-setting"></i>
                        <span>Configuration</span>
                    </template>
                    <el-menu-item-group>
                        <el-menu-item index="1-1">
                            <router-link to="/config">
                                <i class="mdi mdi-key"></i>
                                <span>Namecheap</span>
                            </router-link>
                        </el-menu-item>
                    </el-menu-item-group>
                </el-submenu>
            </el-menu>
        </div>
    </section>
</template>

<script>
    export default {
        name: "app-sidebar"
    }
</script>

<style scoped>


</style>