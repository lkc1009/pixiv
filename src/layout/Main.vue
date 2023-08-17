<script setup lang="ts">
import Carousel from '../components/carousel/Carousel.vue'
import MainCard from '../components/card/MainCard.vue'
</script>

<template>
    <div>
        <el-row class="carousel-card">
            <el-col :span="24">
                <el-row :gutter="20">
                    <el-col :span="16">
                        <Carousel></Carousel>
                    </el-col>
                    <el-col :span="8">
                        <MainCard></MainCard>
                    </el-col>
                </el-row>
            </el-col>
        </el-row>
    </div>
</template>

<style lang="scss" scoped>
.carousel-card {
    height: 200px;
}
</style>
