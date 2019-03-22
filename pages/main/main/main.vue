<template>
	<view class="uni-page-body">
		<!-- 固定在顶部的导航栏 -->
		<page-head :title="title"></page-head>
		<view>
			<view class="content">
				<text class="item_title">查询信息</text>
			</view>
			<view class="uni-flex uni-row content_view">
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="flex-item item_icon"></image>
						<text class="item_name flex-item">我的信息</text>
					</view>
				</view>
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="item_icon flex-item"></image>
						<text class="item_name flex-item">乘车历史</text>
					</view>
				</view>
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="item_icon flex-item"></image>
						<text class="item_name flex-item">缴费历史</text>
					</view>
				</view>
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="item_icon flex-item"></image>
						<text class="item_name flex-item">实时轨迹</text>
					</view>
				</view>
			</view>
			
			<view class="content">
				<text class="item_title">服务办理</text>
			</view>
			<view class="uni-flex uni-row content_view">
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="flex-item item_icon"></image>
						<text class="item_name flex-item">乘车报名</text>
					</view>
				</view>
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="item_icon flex-item"></image>
						<text class="item_name flex-item">缴    费</text>
					</view>
				</view>
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="item_icon flex-item"></image>
						<text class="item_name flex-item">请假管理</text>
					</view>
				</view>
				<view class="flex-item item_view">
					<view class="flex-item uni-flex uni-column">
						<image src="../../../static/logo.png" class="item_icon flex-item"></image>
						<text class="item_name flex-item">提醒服务</text>
					</view>
				</view>
			</view>
			
			<view class="content">
				<text class="item_title">拓展功能</text>
			</view>
			<view class="uni-flex uni-column content_view" style="height: 260upx;">
				<view class="uni-flex uni-row content_view_row">
					<view class="flex-item item_view">
						<view class="flex-item uni-flex uni-column">
							<image src="../../../static/logo.png" class="flex-item item_icon"></image>
							<text class="item_name flex-item">路线定制</text>
						</view>
					</view>
					<view class="flex-item item_view">
						<view class="flex-item uni-flex uni-column">
							<image src="../../../static/logo.png" class="item_icon flex-item"></image>
							<text class="item_name flex-item">订    餐</text>
						</view>
					</view>
					<view class="flex-item item_view">
						<view class="flex-item uni-flex uni-column">
							<image src="../../../static/logo.png" class="item_icon flex-item"></image>
							<text class="item_name flex-item">隐患上报</text>
						</view>
					</view>
					<view class="flex-item item_view">
						<view class="flex-item uni-flex uni-column">
							<image src="../../../static/logo.png" class="item_icon flex-item"></image>
							<text class="item_name flex-item">通    知</text>
						</view>
					</view>
				</view>
				<view class="uni-flex uni-row content_view_row">
					<view class="flex-item item_view">
						<view class="flex-item uni-flex uni-column">
							<image src="../../../static/logo.png" class="flex-item item_icon"></image>
							<text class="item_name flex-item">留言反馈</text>
						</view>
					</view>
					
				</view>
			</view>
		</view>
	</view>
	
</template>

<script>
	export default {
		data() {
			return {
				title:'童泰智慧校车'
			};
		}
	}
</script>

<style>
	.content {
		text-align: center;
	}
	.content_view {
		background: #FFFFFF;
		height:130upx;
		border:1px dashed black;
		border-radius:10px;
		margin-left: 70upx;
		margin-right: 70upx;
		margin-top: 20upx;
		margin-bottom: 20upx;
		line-height: 200px;
		display: flex;
		justify-content:center;
		align-items:Center;
	}
	.content_view_row {
		width: 100%;
		height:130upx;
		display: flex;
		align-items:Center;
	}
	.item_view {
		width: 25%;
	}
	.item_title {
		height: 400upx;
		font-size: 20px;
		color: #007AFF;
		}
	.item_icon {
		align-self: center;
		height: 40upx;
		width: 40upx;
		margin: 5upx;
	}
	.item_name {
		margin: 5upx;
		align-self: center;
		size: 7upx;
	}
</style>
