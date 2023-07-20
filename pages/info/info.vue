<template>
	<view class="nav">
		<view class="header">
			<img src="../../static/image/m1.png" alt="" class="image">
		</view>
			<view class="content">
				<ul v-for="(page, index) in pages" :key="index" @click="pageClick(page.path)"> 
					<li class="list"><span class="message">{{page.title}} </span> <span class="mark">></span></li>
				</ul>
			</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {	
				pages: [
					{
						id: 1,
						title: '修改资料',
						path: '/pages/changeData/changeData'
					},
					{
						id: 2,
						title: '学习记录',
						path: '/pages/learnRecord/learnRecord'
					},
					{
						id: 3,
						title: '我的成绩',
						path: '/pages/score/score'
					},
					{
						id: 4,
						title: '训练记录',
						path: '/pages/trainLearn/trainLearn'
					},
					{
						id: 5,
						title: '我的证书',
						path: '/pages/certificate/certificate'
					},
					{
						id: 6,
						title: '积分日志',
						path: '/pages/scoreLog/scoreLog'
					},
					{
						id: 7,
						title: '密码安全',
						path: '/pages/passwordSafe/passwordSafe'
					},
					{
						id: 8,
						title: '退出登录',
						path: '/pages/logOut/logOut'
					}
				]
			}
		},
		methods: {
			pageClick(url) {
				uni.navigateTo({
					url
				})
			}
		}
	}
</script>

<style>
.header {
	width: 750rpx;
	height: 300rpx;
}

.image {
	width: 750rpx;
	height: 300rpx;
}

.content {
	font-size: 20px;
}

.content .message {
	margin: 15rpx;
	font-size: 35rpx;
	line-height: 30px;
}

.content .mark {
	margin-top: 5px;
	margin-right: 20px;
	color: #BABABA;
}

.content .list{
	display: flex;
	justify-content: space-between;
	margin: 15x 0px;
	border-bottom: solid 1px gainsboro;
}
</style>
