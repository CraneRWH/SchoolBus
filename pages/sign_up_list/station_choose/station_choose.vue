<template>
	<view class="mpvue-picker">
		<!-- 固定在顶部的导航栏 -->
		<uni-nav-bar :fixed="true" :status-bar="true" left-icon="back" @click-left="back" 
		 title="选择上下车站点"></uni-nav-bar>
		 <view class="uni-column item_view">
			 <text class="item_text">请选择校车公司</text>
			 <view class="uni-row select_list" @click="showSinglePicker()">
				  <text class="select_text">{{company}}</text>
				  <image class="select_img" src="../../../static/arrow_down_gray.png"></image>
			 </view>
		 </view>
		 <view class="uni-column item_view">
			 <text class="item_text">上车站点</text>
			 <view class="uni-row select_list" @click="showStationPicker()">
				  <text class="select_text">{{station}}</text>
				  <image class="select_img" src="../../../static/arrow_down_gray.png"></image>
			 </view>
		 </view>
		 <view class="uni-column item_view">
			 <text class="item_text">学校</text>
			 <view class="uni-row select_list" @click="showSchoolPicker()()">
				  <text class="select_text">{{school}}</text>
				  <image class="select_img" src="../../../static/arrow_down_gray.png"></image>
			 </view>
		 </view>
		 <mpvue-picker :themeColor="themeColor" ref="mpvuePicker" :mode="mode" :deepLength="deepLength" :pickerValueDefault="pickerValueDefault"
		  @onConfirm="onConfirm" @onCancel="onCancel" :pickerValueArray="pickerValueArray"></mpvue-picker>
	</view>
</template>

<script>
	import mpvuePicker from '../../../components/mpvue-picker/mpvuePicker.vue';
	export default {
		components: {
			mpvuePicker
		},
		data() {
			return {
				pickerSingleArray: [{
						label: '历城区第一校车公司',
						value: 1,
						type : 1
					},
					{
						label: '高新区第二校车公司',
						value: 2,
						type : 1
					},
					{
						label: '市中区第一校车公司',
						value: 3,
						type : 1
					},
					{
						label: '槐荫区第四校车公司',
						value: 4,
						type : 1
					},
					{
						label: '历城区第一校车公司',
						value: 5,
						type : 1
					},
					{
						label: '高新区第二校车公司',
						value: 6,
						type : 1
					},
					{
						label: '市中区第一校车公司',
						value: 7,
						type : 1
					},
					{
						label: '槐荫区第四校车公司',
						value: 8,
						type : 1
					}
				],
				pickerStationArray: [{
						label: '齐鲁软件园',
						value: 1,
						type : 2
					},
					{
						label: '银河大厦',
						value: 2,
						type : 2
					},
					{
						label: '开拓路与新泺大街交叉口',
						value: 3,
						type : 2
					},
					{
						label: '世纪大道西口',
						value: 4,
						type : 2
					},
					{
						label: '炼油厂路',
						value: 5,
						type : 2
					},
					{
						label: '安家',
						value: 6,
						type : 2
					},
					{
						label: '唐冶街道',
						value: 7,
						type : 2
					},
					{
						label: '绿地城',
						value: 8,
						type : 2
					}
				],
				pickerSchoolArray: [{
						label: '实验小学',
						value: 1,
						type : 3
					},
					{
						label: '唐冶小学',
						value: 2,
						type : 3
					},
					{
						label: '光明小学',
						value: 3,
						type : 3
					},
					{
						label: '平安小学',
						value: 4,
						type : 3
					},
					{
						label: '济大附属小学',
						value: 5,
						type : 3
					},
					{
						label: '炼油厂私立小学',
						value: 6,
						type : 3
					},
					{
						label: '安家小学',
						value: 7,
						type : 3
					},
					{
						label: '唐冶中学',
						value: 8,
						type : 3
					}
				],
				mode: '',
				deepLength: 1,
				pickerValueDefault: [0],
				pickerValueArray:[],
				
				company:'',
				station:'',
				school:''
			};
		},
		methods: {
			onCancel(e) {
				console.log(e)
			},
			// 单列
			showSinglePicker() {
				this.pickerValueArray = this.pickerSingleArray
				this.mode = 'selector'
				this.deepLength = 1
				this.pickerValueDefault = [0]
				this.$refs.mpvuePicker.show()
			},
			showStationPicker() {
				this.pickerValueArray = this.pickerStationArray
				this.mode = 'selector'
				this.deepLength = 1
				this.pickerValueDefault = [0]
				this.$refs.mpvuePicker.show()
			},
			showSchoolPicker() {
				this.pickerValueArray = this.pickerSchoolArray
				this.mode = 'selector'
				this.deepLength = 1
				this.pickerValueDefault = [0]
				this.$refs.mpvuePicker.show()
			},
			onConfirm(e) {
				var result = JSON.stringify(e);
				console.log(e)
				switch (JSON.parse(result).type){
					case 1:
						console.log(JSON.parse(result).type);	
						this.company = JSON.parse(result).label;
						break;
					case 2:
					console.log(JSON.parse(result).type);
						this.station = JSON.parse(result).label;
						break;
					case 3:
					console.log(JSON.parse(result).type);
						this.school = JSON.parse(result).label;
						break;
					default:
					console.log(JSON.parse(result).type);
						break;
				}
			}
		}
	}
</script>

<style>
	.item_view {
		width: 100%;
		display:flex;
		vertical-align: middle;
	}
	
	.item_text {
		height: 50upx;
		line-height:50upx;
		font-size:28upx;
		vertical-align: middle;
		flex: 1;
		margin: 20upx;
	}
	.select_list {
		border: 4upx solid #BEBEBE ;
		height: 70upx;
		flex: 1;
		display: flex;
		align-items: center;
		margin:0upx 20upx;
	}
	.select_text {
		height: 50upx;
		line-height:50upx;
		font-size:28upx;
		vertical-align: middle;
		flex: 1;
		margin: 15upx;
	}
	.select_img {
		height: 50upx;
		width: 50upx;
		margin: 10upx;
	}
</style>
