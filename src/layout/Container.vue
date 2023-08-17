<script setup lang="ts">
import Header from './Header.vue'
import Main from './Main.vue'
import Footer from './Footer.vue'
</script>

<template>
    <div>
        <el-container class="container">
            <el-affix target=".container">
                <el-header>
                    <Header></Header>
                </el-header>
            </el-affix>
            <el-main>
                <Main></Main>
            </el-main>
            <el-footer><Footer></Footer></el-footer>
        </el-container>
    </div>
</template>

<style lang="scss" scoped>
.el-header {
    padding: 0;
    height: 60px;
    line-height: 60px;
}
</style>
