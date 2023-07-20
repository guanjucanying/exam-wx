<template>
	<view class="change">
		<view class="oldPassword" >
			<text>旧密码</text><input type="text" placeholder="输入旧密码">
		</view>
		<view class="newPassword">
			<text>新密码</text><input type="text" placeholder="输入新密码">
		</view>
		<view class="ackPassword">
			<text>确定密码</text><input type="text" placeholder="输入确认密码">
		</view>
		<button type="primary">提交修改</button>
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

<style>
.change view {
	display: flex;
	justify-content: space-between;
	margin-top: 40rpx;
}
.change input {
	height: 60rpx;
	width: 400rpx;
	font-size: 20rpx;
	display: inline-block;
	border: solid 1rpx gainsboro;
	margin-right: 40rpx;
	padding-left: 10rpx;
}
.change text {
	line-height: 60rpx;
	margin-left: 40rpx;
}
.ackPassword {
	margin-bottom: 40rpx;
}

</style>
