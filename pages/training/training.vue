<template>
	<view class="training">
		<view class="content" v-for="item in 10">
			<examList></examList>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
 .content{
	  width: 100%;
	  padding: 30rpx 0;
  }
</style>
