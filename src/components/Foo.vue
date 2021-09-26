<template>
    <view>Component Foo</view>
</template>

<script lang="ts">
import {defineComponent} from 'vue'
import {onHide, onShow} from "@dcloudio/uni-app";

export default defineComponent({
    name: "Foo",
    setup() {
        onShow(() => {
            console.log("onComponentShow")
        })

        onHide(() => {
            console.log("onComponentHide")
        })
    }
})
</script>
