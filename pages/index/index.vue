<template>
	<view>
		<view class="index-swiper">
			<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval"
				:duration="duration">
				<swiper-item>
					<image src="https://xiaohei-1313160286.cos.ap-chengdu.myqcloud.com/img/1a20aa92cdca4c3b7776f7d9be2eec06.png" lazy-load=true mode=""></image>
				</swiper-item>
				<swiper-item>
					<image src="https://xiaohei-1313160286.cos.ap-chengdu.myqcloud.com/img/57f396728e094573bd0b18713e5ce53a.jpg" lazy-load=true mode=""></image>
				</swiper-item>
				<swiper-item>
					<image src="https://xiaohei-1313160286.cos.ap-chengdu.myqcloud.com/img/d7c1c13bf8883f153dc4d2fb7f26e3ea.jpg" lazy-load=true mode=""></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="index-main">
			<view class="index-main-item border-radius-right-down">
				<navigator url="../study/study" open-type="switchTab" hover-class="other-navigator-hover">
					<image src="../../static/icon/study.png" mode=""></image>
					<text class="card-actions-item-text">课程学习</text>
				</navigator>
			</view>
			<view class="index-main-item border-radius-left-down" >
				<navigator url="../exam/exam" open-type="switchTab" hover-class="other-navigator-hover">
					<image src="../../static/icon/selectexam.png" mode=""></image>
					<text class="card-actions-item-text">在线考试</text>
				</navigator>
			</view>
			<view class="index-main-item border-radius-right-up">
				<navigator url="../training/training" open-type="switchTab" hover-class="other-navigator-hover">
					<image src="../../static/icon/training.png" mode=""></image>
					<text class="card-actions-item-text">题库训练</text>
				</navigator>
			</view>
			<view class="index-main-item border-radius-left-up">
				<navigator url="../competition/competition" open-type="navigate" hover-class="other-navigator-hover">
					<image src="../../static/icon/info.png" mode=""></image>
					<text class="card-actions-item-text">知识竞赛</text>
				</navigator>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500
			}
		},
		methods: {

		}
	}
</script>

<style>
	.index-swiper {
		width: 690rpx;
		width: 100%;
	}
	.swiper {
		height: 300rpx;
	}
	.swiper image{
		width: 100%;
		height: 100%;
	}
	.index-main{
		width: 100%;
		padding: 50rpx;
		box-sizing: border-box;
		display: grid;
		grid-template-columns: auto auto; 
		grid-template-rows: 200rpx 200rpx;
		grid-gap: 30rpx;
		
	}
	.index-main-item{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		box-shadow: 5rpx 5rpx 10rpx 8rpx rgba(219, 238, 254, 0.5);
	}
	.index-main-item navigator{
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.border-radius-right-down{
		border-radius: 5px 5px 15px 5px;
	}
	.border-radius-left-down{
		border-radius: 5px 5px 5px 15px;
	}
	.border-radius-right-up{
		border-radius: 5px 15px 5px 5px;
	}
	.border-radius-left-up{
		border-radius: 15px 5px 5px 5px;
	}
	.index-main-item image{
		width: 40px;
		height: 40px;
		display: block;
	}
</style>
