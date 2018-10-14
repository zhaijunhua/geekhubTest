<template>
    <div class="header" id="header">
        <el-row class="nav">
            <el-col>
                <div class="topBar">
                    <el-row>
                        <el-col>
                             <el-menu
                                :default-active="activeIndex"
                                class="el-menu-demo"
                                mode="horizontal"
                                background-color="#545c64"
                                text-color="#fff"
                                active-text-color="#ffd04b"
                                @select="handleSelect" unique-opend router>
                                    <el-menu-item index="/" class="logo"><logo/></el-menu-item>
                                    <el-menu-item index="/">首页</el-menu-item>
                                    <el-menu-item index="download">下载</el-menu-item>
                                    <el-menu-item index="resource">资源</el-menu-item>
                                    <el-menu-item index="blog">博客</el-menu-item>
                            </el-menu>
                        </el-col>
                    </el-row>
                </div>
            </el-col>
            <div class="container">
                <router-view></router-view>
            </div>
            
            
        </el-row>
    </div>
    
</template>
<script>
import logo from './logo.vue';
import Home from './home.vue';
import Download from './download.vue';
import Resource from './resource/resource.vue';
import Blog from './blogs/blog.vue';
export default {
    name: 'Header',
    data() {
        return {};
    },
    components: {
        logo,
        Download,
        Home,
        Resource,
        Blog
    },
    methods: {
        handleSelect(key, keyPath) {
            console.log(key, keyPath);
        }
    },
    computed: {
        activeIndex() {
            return this.$route.path.replace('/', '');
        }
    }
};
</script>
<style lang="scss" scoped>
#header{
    width: 100%;
}
    .logo{
       &:hover{
            background-color: #545c64;
        }
    }
</style>

