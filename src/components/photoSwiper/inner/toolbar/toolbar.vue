<template>
    <div id="Player-toolbar">
        <button id="toolbar-zoomIn" class="iconfont iconsrt-enlarge1" @click="zoomIn"></button>
        <button id="toolbar-zoomOut" class="iconfont iconsrt-narrow1" @click="zoomOut"></button>
        <button id="toolbar-rotate-ccw" class="iconfont iconsrt-anti-clockwise1" @click="rotateCCW"></button>
        <button id="toolbar-rotate-cw" class="iconfont iconsrt-clockwise1" @click="rotateCW"></button>
        <button id="toolbar-play" style="display: none"></button>
    </div>
</template>

<script>
    export default {
        methods: {
            zoomIn() {
                this.$emit('zoomIn');
            },
            zoomOut() {
                this.$emit('zoomOut');
            },

            rotateCCW() {
                this.$emit('rotateCCW');
            },
            rotateCW() {
                this.$emit('rotateCW');
            },
        }
    }
</script>

<style lang="stylus" scoped>
    @import "../../mixins.styl"

    #Player-toolbar
        top: 20px
        right: 60px

        button
            width: 40px
            height: 40px
            border: 0
            border-radius: 50%
            font-size: 20px
            color: #FFF
            background-color: rgba(85, 85, 85, 0.4)
            margin-left: 6px
            cursor: pointer

            &:hover
                background-color: rgba(85,85,85,1)
</style>