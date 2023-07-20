<template>
	<view class="study">
		<!-- 搜索部分 -->
		<view class="search">
			<image src="../../static/icon/search.png"></image>
			<input placeholder="搜索课程"/>
		</view>
		<view class="nav-bar">
			<!-- 导航栏 -->
	        <view class="item"
			:class="index == navIndex ? 'active' :''"
			 v-for="(index,item) in 4"
			 @click="clickNav(index)">
	        	全部
	        </view>
	
		</view>
		<view class="content" v-for="item in 10">
			<examList></examList>
		</view>
	</view>
</template>


<script>
	export default {
		data() {
			return {
				navIndex:1
			}
		},
		methods: {
			clickNav(index){
				this.navIndex=index;
			}
		}
	}
</script>

<style lang="scss">
  .search{
	  width: 80%;
	  height: 60rpx;
	  margin: 30rpx auto;
	  border-radius: 100rpx;
	  display: flex;
	  align-items: center;
	  text-align: center;
	  background-color: #F8F8F8;
	  
	  image{
	  	  width: 50rpx;
	  	  height: 50rpx;
	  	  display: inline-block;
	  	  margin-left: 30rpx;
	  }
	  input{
	  	  width: 80%;
	  	  height: 40rpx;
	  	  display: inline-block;
	  	  text-align: left;
	  	  vertical-align: middle;
	  	  background-color: #F8F8F8;
	  
	  }
  }
  .nav-bar{
	  display: flex;
	  justify-content: center;
	  background-color: #F5F5F5;
	  padding: 20rpx 0 4px 0;
	  margin-bottom: 2rpx solid #a4a4a5;
	  .item{
		  flex: 1;
		  text-align: center;
		  padding-bottom: 15rpx;
		 &.active{
			  border-bottom: 2px solid #0279FF;
		 }
	  }
  }
  .content{
	  width: 100%;
	  padding: 30rpx 0;
  }
</style>
