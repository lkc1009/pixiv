<script setup lang="ts">
import { ref } from 'vue'
import { Search } from '@element-plus/icons-vue'

const defaultActive = ref('1')
const changeActive = (key: string, keyPath: string) => {
    console.log(key, keyPath)
}

const logoClick = () => {
    console.log('logoClick')
}

const logoSrc = ref(
    'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg'
)

const search = ref('')
const clickSearch = () => {
    console.log('search')
}
</script>

<template>
    <div>
        <el-menu
            :default-active="defaultActive"
            mode="horizontal"
            :ellipsis="false"
            @select="changeActive"
        >
            <el-menu-item index>
                <img :src="logoSrc" @click="logoClick" />
            </el-menu-item>
            <div class="flex-grow" />
            <el-menu-item index class="search">
                <el-input v-model="search" placeholder="请输入内容">
                    <template #suffix>
                        <el-icon class="el-input__icon">
                            <Search class="search-icon" @click="clickSearch" />
                        </el-icon>
                    </template>
                </el-input>
            </el-menu-item>
            <el-menu-item index="2">登录</el-menu-item>
            <el-menu-item index="3">注册</el-menu-item>
        </el-menu>
    </div>
</template>

<style lang="scss" scoped>
div,
.el-menu,
img {
    height: 100%;
}
.el-menu {
    .el-menu-item {
        border-bottom: 0;
    }
    .el-menu-item:first-child {
        padding: 5px 0;
    }
    .el-menu-item:nth-child(3) {
        padding: 8px;
        :deep(.el-input .el-input__wrapper.is-focus) {
            box-shadow: 0 0 0 1px #c0c4cc inset;
        }
    }
    .flex-grow {
        flex-grow: 1;
    }
    .search {
        .search-icon:hover {
            cursor: pointer;
        }
    }
}
.el-menu--horizontal .el-menu-item:not(.is-disabled):first-child:hover,
.el-menu--horizontal .el-menu-item:not(.is-disabled):nth-child(3):hover {
    background-color: white;
}
.el-menu--horizontal > .el-menu-item.is-active {
    border-bottom: 0;
}

@media screen and (max-width: 768px) {
    .search {
        visibility: hidden;
    }
}
</style>
