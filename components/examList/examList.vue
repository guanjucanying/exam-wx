<template>
	<view class="examList">
		<view class="text">
			<!-- 标题 -->
			<view class="title">
				{{item.title}}
			</view>
			<view class="info" v-if="!item.num">
				<text>类型：{{item.type}}</text>
			</view>
			<view class="info" v-else>
				<text>{{item.num}}道题</text>
			</view>
		</view>
		<view class="limit-time" v-if="!item.type">
			<text>{{item.limitTime}}</text>
		</view>
		<view class="pic">
		     <image src="../../static/icon/right.png" mode="aspectFill"></image>
		</view>
	</view>
</template>

<script>
	export default {
		name:"examList",
		props:{
			item:{
				type:Object,
				default(){
					return {
						title:"【云帆课程】默认标题默认标题默认标题默认标题默认标题默认标题默认标题默认标题",
						type:"职业技能",
						// num:999,
						limitTme:"不限时"
					}
				}
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.examList{
		display: flex;
		flex-direction: row;
		align-items: center;
		padding:0 25rpx 25rpx 25rpx;
		border-bottom: 1px solid #F5F5F5;
		.text{
			width: 100%;
			display: flex;
			flex-direction: column;
			.title{
				font-size: 38rpx;
				padding: 0 45rpx 10rpx 0;
				// padding-bottom: 10rpx;
				line-height: 60rpx;
				word-wrap:break-word;
				word-break:normal; 
				// 超过两行的时候显示省略号
				text-overflow: -o-ellipsis-lastline;
				overflow: hidden;   //溢出内容隐藏
				text-overflow: ellipsis;   //文本溢出部分用省略号表示
				display: -webkit-box;    //显示特别模式
				-webkit-line-clamp: 2;   //表示行数
				line-clamp: 2;   
				-webkit-box-orient: vertical;  //盒子中内容竖直排列
			}
			.info{
				font-size: 32rpx;
				color: #999;
			}
		}
		.limit-time{
			width: 135rpx;
			height: 100%;
		}
		.pic{
			width: 30rpx;
			height: 30rpx;
			image{
				width: 100%;
				height: 100%;
			}
		}
		
	}

</style>