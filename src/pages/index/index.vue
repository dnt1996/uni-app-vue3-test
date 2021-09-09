<template>
	<view>
        <!--只在页面代码中并且嵌套了任何组件都会无法触发click事件-->
        <Wrapper>
            <ScopedSlotComponent v-slot="{item}">
                <view @click="onClick">
                    {{item}}
                </view>
            </ScopedSlotComponent>
        </Wrapper>

        <!--不嵌套则正常触发-->
        <ScopedSlotComponent v-slot="{item}">
            <view @click="onClick">
                {{item}}
            </view>
        </ScopedSlotComponent>
	</view>
</template>

<script>
	import ScopedSlotComponent from "../components/ScopedSlotComponent";
    import Wrapper from "../components/Wrapper";
    export default {
        components: {
            Wrapper,
            ScopedSlotComponent
        },
        setup() {
            return {
                title: true,
                onClick: console.log
            }
        },
	}
</script>
