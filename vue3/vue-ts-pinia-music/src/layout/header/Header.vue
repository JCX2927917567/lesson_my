<template>
    <header class="header" :class="`${themeType}-bg-primary_1`">
        <div class="header-title">
        <i class="iconfont icon-music" :class="`${themeType}-cl-primary_1`"></i>
            <span class="header-title_name">好 听 音 乐</span>
        </div>
        <div class="header-history">
            <i class="iconfont icon-preview-left" :class="`${themeType}-bg-primary_2`" @click="handleBack"></i>
            <i class="iconfont icon-preview-right" :class="`${themeType}-bg-primary_2`" ></i>
        </div>
        <div class="header-input">
            <!-- <search-list/> -->
        </div>
        <div class="header-options">
            <i class="iconfont icon-set"></i>
            <i class="iconfont icon-theme" @click="themeStore.changeTheme()"></i>
        </div>
    </header>
</template>

<script setup lang="ts">
import { computed } from 'vue';
import { useThemeStore } from '@/store/theme'

const themeStore = useThemeStore()
const themeType = computed(() => themeStore.theme) // ThemeStore
const handleBack = () => {}
</script>

<style lang="stylus" scoped>
@import '../../assets/css/variables.styl';
.header {
        position: fixed;
        top: 0;
        right: 0;
        left: 0;
        z-index: 5;
        display: flex;
        height: $header-height;
        padding: 0 20px;
        color: #f2f3f4;
        align-items: center;
        .header-title {
            flex: 0 0 200px;
            .icon-music {
                padding: 4px;
                margin-right: 10px;
                font-size: 20px;
                font-weight: 700;
                background: #f2f3f4;
                border-radius: 50%;
            }
            .header-title_name {
                font-size: 18px;
            }
        }
        .header-history {
            flex: 0 0 100px;
            text-align: center;
            .iconfont {
                padding: 4px;
                margin: 0 4px;
                font-size: 16px;
                cursor: pointer;
                border-radius: 50%;
            }
        }
        .header-options {
            flex: 0 0 100px;
            .iconfont {
                margin: 0 8px;
                font-size: 20px;
                cursor: pointer;
            }
        }
    }
</style>