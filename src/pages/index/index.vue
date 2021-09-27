<template>
	<view>
        <!--正常渲染-->
        <Foo name="Bar"></Foo>

        <!--name=""-->
		<Foo
            :name="list.toString()"
        ></Foo>

        <!--完全不渲染-->
        <Foo
            v-for="item in list"
            :key="item.id"
            :name="item.id.toString()"
        ></Foo>
	</view>
</template>

<script>
	import Foo from "./Foo";
    export default {
        components: {Foo},
        setup() {
            return {
                list: [
                    {id: 1},
                    {id: 2},
                    {id: 3}
                ],
            }
        }
	}
</script>

