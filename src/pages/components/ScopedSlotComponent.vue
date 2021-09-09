<template>
    <view>
        <slot :item="item"></slot>
    </view>
</template>

<script>
export default {
    setup() {
        return {
            item: 1
        }
    }
}
</script>
