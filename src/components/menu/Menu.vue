<template>
    <el-row>
        <el-col :span="12">
            <el-menu
                    default-active="2"
                    class="el-menu-vertical-demo"
                    @open="handleOpen"
                    @close="handleClose"
                    background-color="#545c64"
                    text-color="#fff"
                    active-text-color="#ffd04b">
                <MenuItem v-for="item in menuItems" :key="item.key" :menu-item="item"/>
            </el-menu>
        </el-col>
    </el-row>
</template>

<script>
import MenuItem from "@/components/menu/MenuItem.vue";
export default {
    name: "Menu",
    components: {MenuItem},
    data() {
        return {
            "menuItems": [
                {
                    key: "one",
                    name: "导航1",
                    icon: "location",
                    index: "1",
                    children: [
                        {
                            key: "one-one",
                            name: "导航1 - 1",
                            icon: "setting",
                            index: "1-1"
                        }
                    ]
                },
                {
                    key: "two",
                    name: "导航2",
                    icon: "star-on",
                    index: "2",
                }
            ]
        }
    },
    methods:  {
        handleOpen(key, keyPath) {
            console.log(key, keyPath);
        },
        handleClose(key, keyPath) {
            console.log(key, keyPath);
        }
    }
}
</script>

<style scoped>

</style>