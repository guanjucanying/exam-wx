<template>
	<view>
		<uni-card v-for="(certificate, index) in credentials" :key="index">
			<view class="card" >
				<view class="header">
					{{certificate.name}}
				</view>
				<view class="content">
					<p>获得时间：{{certificate.getTime}}</p>
					<p>取得方式：{{certificate.getWay}}</p>
					<p>颁发机构：{{certificate.authority}}</p>
					<p>到期时间：{{certificate.deadline}}</p>
					<p>证书类别：{{certificate.category}}</p>
				</view>
			</view>
		</uni-card>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				 credentials:[
					 {
						 id: 1,
						 name: "北京云帆证书",
						 getTime: "2022-11-21 18:36:40",
						 getWay: "人工颁发",
						 authority: "北京云帆",
						 deadline: "2027-11-21 18:36:40",
						 category: "计算机等级证书"
					 },
					 {
						 id: 1,
						 name: "北京云帆证书",
						 getTime: "2022-11-21 18:36:40",
						 getWay: "人工颁发",
						 authority: "北京云帆",
						 deadline: "2027-11-21 18:36:40",
						 category: "计算机等级证书"
					 }
				 ]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.header {
	padding-bottom: 10rpx;
	margin-bottom: 10rpx;
	border-bottom: 1rpx solid gainsboro;
	text-align: center;
}
.content {
	margin: 0 auto;
}
</style>
