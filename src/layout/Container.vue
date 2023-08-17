<script setup lang="ts">
import Header from './Header.vue'
import Main from './Main.vue'
</script>

<template>
    <div>
        <el-container class="container">
            <el-header>
                <Header></Header>
            </el-header>
            <el-main>
                <Main></Main>
            </el-main>
        </el-container>
    </div>
</template>

<style lang="scss" scoped>
div,
.el-container {
    height: 100%;
}
.el-header {
    padding: 0;
    height: 60px;
    line-height: 60px;
}
</style>
