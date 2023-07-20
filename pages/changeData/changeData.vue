<template>
	<view>
		<view class="nav">
			<text>ID</text><input type="text" class="input" v-model="item.id" disabled="disabled">
		</view>
		<view class="nav">
			<text>用户名</text><input type="text" class="input" v-model="item.username" disabled="disabled">
		</view>
		<view class="nav operation">
			<text>用户头像</text>
			<view class="operationImg" >
				<view class="existence" v-if="isHave">
					<view class="">
						<image v-for="li in imgList" :src="li" class="uploadImg"></image>
					</view>
					<view class="delImg">
						<button type="warn" @click="deleteImg">清除</button>
					</view>
				</view>
				<view class="non-existent" v-else>
					<view class="uploadBtn">
						<button type="primary" @click="postImg">上传</button>
					</view>
				</view>
			</view>
		</view>
		<view class="nav">
			<text>用户照片</text>
			<view class="alawaysBtn">
				<button type="primary" @click="postImg">上传</button>
			</view>
		</view>
		<view class="nav">
			<text>姓名</text><input type="text" class="input" v-model="item.name">
		</view>
		<view class="nav">
			<text>身份证号</text><input type="text" class="input" v-model="item.idNumber">
		</view>
		<view class="nav">
			<text>手机号</text>
			<text class="phone">{{item.phoneNumber}}</text><button type="warn">解绑</button>
		</view>
		<view class="nav">
			<text>邮箱</text><input type="text" class="input" v-model="item.mailbox">
		</view>
		<view class="navSave">
			<button type="primary" class="save">保存资料</button>			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgList: [],
				isHave: false,
				item: {
					id: 12345678,
					username: "student",
					name: "学员A",
					idNumber: 5000,
					phoneNumber: 18603038204,
					mailbox: "1234567@qq.com"
				},
			}
		},
		methods: {
			postImg() {
				uni.chooseImage({
					count: 2,
					success:res => {
						this.imgList = [...res.tempFilePaths];
						this.isHave = true;
					}
				})
			},
			deleteImg() {
				this.imgList = "";
				this.isHave = false;
			}
		}
	}
</script>

<style>
.nav {
	display: flex;
	justify-content: space-between;
	padding: 0 60rpx;
	margin: 40rpx 0;
}
.nav text {
	line-height: 40rpx;
	padding: 20rpx;
}
.input {
	border: 1px solid #eee;
	border-radius: 10rpx;
	width: 350rpx;
	height: 70rpx;
	padding: 10rpx;
}
.save {
	width: 650rpx;
}
.delImg {
	width: 130rpx;
	height: 100rpx;
	margin-left: 10rpx;
}
.uploadImg {
	width: 200rpx;
	height: 300rpx;
}

.alawaysBtn {
	margin-right: 240rpx;
}

.non-existent .uploadBtn{
	margin-right: 60rpx;
}

.operation {
	margin-right: 180rpx;
}
.phone {
	margin-left: 100rpx;
}
</style>
