<script setup lang="ts"></script>

<template>
    <div class="card">
        <el-card class="box-card">
            <template #header>
                <div class="card-header">
                    <span>Card name</span>
                    <el-button class="button" text>Operation button</el-button>
                </div>
            </template>
            <div v-for="o in 4" :key="o" class="text item">
            </div>
        </el-card>
    </div>
</template>

<style lang="scss" scoped>
.card, .box-card {
    height: 100%;
}
.card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.text {
    font-size: 14px;
}

.item {
    margin-bottom: 18px;
}

.box-card {
    width: 480px;
}
</style>
