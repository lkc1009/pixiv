<script setup lang="ts">

</script>

<template>
    <div class="card">
        <el-card class="box-card" shadow="never">
            <div v-for="o in 4" :key="o" class="text item">{{ o }}</div>
        </el-card>
    </div>
</template>

<style lang="scss" scoped>
.card,
.box-card {
    height: 100%;
    .card-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
}
</style>