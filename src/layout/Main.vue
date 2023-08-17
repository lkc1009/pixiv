<script setup lang="ts">
import Carousel from '../components/carousel/Carousel.vue'
import NoticeCard from '../components/card/NoticeCard.vue'
import WarnNotice from '../components/notice/WarnNotice.vue'
import RankCard from '../components/card/RankCard.vue'
import ComicCard from '../components/card/ComicCard.vue'
</script>

<template>
    <div>
        <el-row class="warn-notice">
            <el-col :span="24">
                <WarnNotice></WarnNotice>
            </el-col>
        </el-row>
        <el-row class="carousel-card">
            <el-col :span="24">
                <el-row :gutter="20">
                    <el-col :span="16">
                        <Carousel></Carousel>
                    </el-col>
                    <el-col :span="8">
                        <NoticeCard></NoticeCard>
                    </el-col>
                </el-row>
            </el-col>
        </el-row>
        <el-row class="rank-card">
            <el-col :span="24">
                <el-row :gutter="20">
                    <el-col :span="18">
                        <RankCard></RankCard>
                    </el-col>
                    <el-col :span="6">
                        <ComicCard></ComicCard>
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
.el-row:not(:first-child, :nth-child(2)) {
    margin-top: 25px;
}
</style>
