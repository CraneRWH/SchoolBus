<template>
	<view>
		<!-- 固定在顶部的导航栏 -->
		<uni-nav-bar :fixed="true" :status-bar="true" left-icon="back" @click-left="back" 
		 title="报名列表"></uni-nav-bar>
		 <view class="uni-list" >
		 	<view class="item_view uni-column"  v-for="(item,index) in lists" :key="index">
				<view class="uni-row item_row" >
					<text class="item_text1">{{item.title}}</text>
					<text class="item_text">{{item.name}}</text>
					<text class="item_right">{{item.status}}</text>
				</view>
				<view class="uni-row item_row">
					<text class="item_text1">{{item.type}}</text>
					<text class="item_text1">{{item.time}}</text>
				</view>
		 		<view class="line_view"></view>
		 	</view>
		 </view>
		 <view class="bottom_v">
		 	<button class="bottom_btn" @click="toStationChoose()">添加报名</button>
		 </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				lists :[
					{
						title : "齐鲁软件园-唐城小区",
						name: "王小明",
						status : "待缴费",
						type:"上学",
						time: "一个月",
					},
					{
						title : "齐鲁软件园-唐城小区",
						name: "王小明",
						status : "待缴费",
						type:"上学",
						time: "一个月",
					},
					{
						title : "齐鲁软件园-唐城小区",
						name: "王小明",
						status : "待缴费",
						type:"上学",
						time: "一个月",
					},
					{
						title : "齐鲁软件园-唐城小区",
						name: "王小明",
						status : "待缴费",
						type:"上学",
						time: "一个月",
					},
				]
			};
		},
		methods:{
			toStationChoose() {
				uni.navigateTo({
					url: 'station_choose/station_choose',
				});
			}
		}
	}
</script>

<style>
	.line_view {
		height: 4upx;
		width: 100%;
		background: #D9D9D9;
		display:flex;
	}
	.item_view {
		width: 100%;
		display:flex;
		vertical-align: middle;
		justify-content: center;
	}
	.item_row{
		flex: 1;
		display: flex;  
		height: 50upx;
		padding: 10upx 20upx;
	}
	.item_text1 {
		height: 50upx;
		font-size:28upx;
		vertical-align: middle;
		margin-right: 50upx;
	}
	.item_text {
		height: 50upx;
		line-height:50upx;
		font-size:28upx;
		vertical-align: middle;
		flex: 1;
	}
	.item_right {
		margin-right: 10upx;
		font-size:28upx;
		display:flex;
		vertical-align: middle;
		color: #F0AD4E;
	}
	.bottom_v {
		width: 100%;
		flex-direction: row;
		position:fixed;  
		bottom:0px;  
		z-index:100;
		height: auto;
		background: #FFFFFF;
	}
	.bottom_btn {
		flex: 1;
		font-size: 32upx;
		background: #0A98D5;
		padding: 1upx;
		color: #FFFFFF;
		height: auto;
		margin: 20upx;
	}
</style>
