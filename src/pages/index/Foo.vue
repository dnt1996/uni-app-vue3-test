<template>
    <view>name: {{ name }}</view>
</template>

<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
    name: "Foo",
    props: {
        name: {
            type: String,
            default: "Foo"
        }
    }
})
</script>
