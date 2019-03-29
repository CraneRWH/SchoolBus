<template>
	<view>
		<uni-nva-bar :fixed="true" :status-bar="true" left-icon="back" 
		@click-left="back" title="家长绑定"></uni-nva-bar>
		<view class="uni-common-mt">
            <view class="uni-form-item uni-row row_item">
                <view class="left_title">姓&#12288&#12288名：</view>
                <input class="uni-input" focus placeholder="请输入姓名" />
            </view>
            <view class="uni-form-item uni-row row_item">
                <view class="left_title">身份证号：</view>
                <input class="uni-input" placeholder="请输入身份证号" />
            </view>
            <view class="uni-form-item uni-row row_item">
                <view class="left_title">密&#12288&#12288码：</view>
                <input class="uni-input" maxlength="18" placeholder="请输入密码" />
            </view>
            <view class="uni-form-item uni-row row_item">
                <view class="left_title">确认密码：</view>
                <input class="uni-input" placeholder="请确认密码" />
            </view>
            <view class="uni-form-item uni-row row_item" style="margin-top: 50upx;">
                <view class="left_title">手机号码：</view>
                <input class="uni-input" type="number" placeholder="请输入手机号码" />
            </view>
			<view class="uni-form-item uni-row row_item">
				<view class="left_title">验&ensp;证&ensp;码：</view>
				<input class="mobile_code_text" type="number" maxlength="6" placeholder="请输入验证码" />
				<button type="primary" class="mobile_code_btn">获取验证码</button>
			</view>
			
			<button type="primary" class="bind_btn">注册并绑定</button>
        </view>
	</view>
</template>

<script>
	import uniNavBar from '../../../components/uni-nav-bar.vue'
	import uniIcon from '../../../components/uni-icon.vue'
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style>
	.row_item {
		align-items:Center;
		padding-left: 40upx;
	}
	.left_title {
		height: 50upx;
		font-size:28upx;
		background:#FFF;
	}
	.mobile_code_text {
		height: 50upx;
		padding: 15upx 25upx;
		line-height:50upx;
		font-size:28upx;
		background:#FFF;
		flex: 1;
		flex-shrink:1;
	}
	.mobile_code_btn {
		font-size:28upx;
		margin-right: 20upx;
	}
	.bind_btn{
		font-size:28upx;
		margin: 50upx;
	}
</style>
