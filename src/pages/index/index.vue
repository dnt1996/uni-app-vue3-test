<template>
	<Foo></Foo>
</template>

<script>
import {onHide, onShareAppMessage, onShow} from "@dcloudio/uni-app";
    import {defineComponent} from "vue";
    import Foo from "../../components/Foo";

    export default defineComponent({
        components: {Foo},
        setup() {
            onShow(() => {
                console.log("onShow")
            })

            onHide(() => {
                console.log("onHide")
            })
        }
    })
</script>
