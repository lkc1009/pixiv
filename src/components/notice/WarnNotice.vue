<script setup lang="ts"></script>

<template>
    <div class="warn tips">
        <p class="tip-title">重要通知</p>
        <p class="content">测试最近功能</p>
    </div>
</template>

<style lang="scss" scoped>
.warn.tips {
    padding: 8px 16px;
    background-color: rgba(64, 158, 255, 0.1);
    border-radius: 4px;
    border-left: 5px solid var(--el-color-primary);
    margin: 20px 0;
    .tip-title {
        margin-top: 0;
        font-weight: 700;
    }
    .content {
        font-weight: 0.9rem;
        margin-bottom: 0;
        line-height: 1.75rem;
    }
}
</style>
