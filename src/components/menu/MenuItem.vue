<template>
    <el-submenu v-if="menuItem.children" :index="menuItem.index">
        <template slot="title">
            <i :class="`el-icon-${menuItem.icon}`"></i>
            <span>{{ menuItem.name }}</span>
        </template>
        <MenuItem v-for="item in menuItem.children" :key="item.key" :menu-item="item"/>
    </el-submenu>
    <el-menu-item v-else :index="menuItem.index" >
        <i :class="`el-icon-${menuItem.icon}`"></i>
        <span slot="title">{{ menuItem.name}}</span>
    </el-menu-item>
</template>

<script>
export default {
    name: "MenuItem",
    props: ["menuItem"]
}
</script>

<style scoped>

</style>