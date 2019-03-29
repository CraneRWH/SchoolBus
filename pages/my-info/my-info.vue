<template>
	<view>
		<uni-nva-bar :fixed="true" :status-bar="true" left-icon="back"
		@click-left="back" title="我的信息"></uni-nva-bar>
		<view class="uni-column">
			<view class="row_item uni-row uni-form-item">
				<text class="left_title">姓名</text>
				<text class="right_text">张大头</text>
			</view>
			<view class="line_view"></view>
			<view class="row_item uni-row uni-form-item">
				<text class="left_title">手机号</text>
				<text class="right_text">18701717003</text>
			</view>
			<view class="line_view"></view>
			<view class="row_item uni-row uni-form-item">
				<text class="left_title">身份证号</text>
				<text class="right_text">37292619860212654X</text>
			</view>
			<view class="line_view"></view>
		</view>
		<view class="uni-column" style="margin-bottom: 150upx;">
			<text class="l_title">我的孩子</text>
			<view class="uni-list" >
				<view class="item_view uni-column"  v-for="(item,index) in lists" :key="index">
					<view class="item_view uni-row" hover-class="uni-list-cell-hover">
						<image class="item_icon" src="../../static/head_icon.png"></image>
						<view class="text_row">
							<view class="uni-row" style="flex: 1;display: flex;  height: 50upx;">
								<text class="item_text">{{item.name}}&nbsp;&nbsp;{{item.sex}}&nbsp;&nbsp;{{item.age}}</text>
								<image src="../../static/delete.png" class="icon_style" mode="scaleToFill"></image>
								<image src="../../static/edit.png" class="icon_style"   mode="scaleToFill" style="margin-right: 20upx;"></image>
							</view>
							<view>{{item.address}}</view>
						</view>
					</view>
					<view class="line_view"></view>
				</view>
			</view>
		</view>
		<view class="bottom_v">
			<button class="bottom_btn">添加孩子</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				lists :[
					{
						name : '王小二',
						sex : '男',
						age :'6岁',
						address : '山东省济南市历城区唐城小学三年级二班'
					},
					{
						name : '王小四',
						sex : '男',
						age :'7岁',
						address : '山东省济南市历城区唐城小学四年级二班'
					},
					{
						name : '王小二',
						sex : '男',
						age :'6岁',
						address : '山东省济南市历城区唐城小学三年级二班'
					},
					{
						name : '王小四',
						sex : '男',
						age :'7岁',
						address : '山东省济南市历城区唐城小学四年级二班'
					},
					{
						name : '王小二',
						sex : '男',
						age :'6岁',
						address : '山东省济南市历城区唐城小学三年级二班'
					},
					{
						name : '王小四',
						sex : '男',
						age :'7岁',
						address : '山东省济南市历城区唐城小学四年级二班'
					},
					{
						name : '王小二',
						sex : '男',
						age :'6岁',
						address : '山东省济南市历城区唐城小学三年级二班'
					},
					{
						name : '王小四',
						sex : '男',
						age :'7岁',
						address : '山东省济南市历城区唐城小学四年级二班'
					},
					]
			};
		}
	}
</script>

<style>
	.row_item {
		align-items:Center;
		padding-left: 40upx;
	}
	.l_title {
		height: 100upx;
		font-size:32upx;
		margin-top: 10upx;
		margin-bottom: 10upx;
		padding: 0upx 40upx;
		display:table-cell;
		vertical-align: middle;
		font-weight: bold;
	}
	.item_view {
		width: 100%;
		display:flex;
		vertical-align: middle;
		justify-content: center;
		align-items: center
	}
	.left_title {
		height: 50upx;
		font-size:28upx;
		line-height:50upx;
	}
	.right_text {
		height: 50upx;
		padding: 15upx 25upx;
		line-height:50upx;
		font-size:28upx;
		flex: 1;
		flex-shrink:1;
		text-align: right;
	}
	.line_view {
		height: 4upx;
		width: 100%;
		background: #D9D9D9;
		display:flex;
	}
	.icon_style {
		width: 40upx;
		height: 40upx;
		margin-right: 20upx;
	}
	.item_text {
		height: 50upx;
		line-height:50upx;
		font-size:28upx;
		flex: 1;
	}
	.item_icon {
		width: 80upx;
		height: 80upx;
		margin-left: 10upx;
		margin-right: 10upx;
		display:flex;
		align-items: center;
	}
	.text_row {
		flex-direction: column;
		line-height: 50upx;
		margin: 10upx;
		vertical-align: middle;
		flex: 1;
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
