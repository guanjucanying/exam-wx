<template>
	<view>
		<template v-for="(value,index) in knowcards">
			<uni-card>
				<view class="know-img">
					<image :src="value.know_img" alt=""></image>
				</view>
				<view class="know-title">
					{{value.know_title}}
				</view>
				<view class="know-time">
					<span>活动时间：</span>
					<span>{{value.know_time_begin}}~{{value.know_time_end}}</span>
				</view>
				<view class="know-ways">
					<span>参与方式：</span>
					<span>{{value.know_ways}}</span>
				</view>
				<view class="know-status">
					<span>竞赛状态：</span>
					<span>{{value.know_tatus}}</span>
				</view>
			</uni-card>
		</template>
	</view>
</template>

<script setup>
import { reactive } from "vue";
const knowcards = reactive([
	{
		know_img:'https://xiaohei-1313160286.cos.ap-chengdu.myqcloud.com/img/1a20aa92cdca4c3b7776f7d9be2eec06.png',
		know_title:'每日知识竞赛',
		know_time_begin:"2020/10/20",
		know_time_end:"2020/11/30",
		know_ways:"每天5次",
		know_tatus:1
	},
	{
		know_img:'https://xiaohei-1313160286.cos.ap-chengdu.myqcloud.com/img/1a20aa92cdca4c3b7776f7d9be2eec06.png',
		know_title:"每日知识竞赛",
		know_time_begin:"2020/10/20",
		know_time_end:"2020/11/30",
		know_ways:"每天5次",
		know_tatus:1
	}
])
</script>

<style>
	.know-img{
		width: 100%;
		height: 100px;
	}
	.know-img image{
		width: 100%;
		height: 100%;
	}
	.know-title{
		font-size: 15px;
		color: black;
		margin: 3px;
	}
</style>
