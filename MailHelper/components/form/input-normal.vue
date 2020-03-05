<template>
	<view class="text-input">
		<text class="inputLabel">{{inputLabel}}：</text>
		<input id="username" type="text" name="username" :placeholder="phHolder"/>
	</view>
</template>

<script>
	export default{
		name:"inputNormal",
		props:{
			inputLabel: String,
			phHolder:String
		}
	}
</script>

<style scoped>
	.text-input{
		width: 100%;
		display: flex;
		flex-wrap: nowrap;
		justify-content: center;
		align-items: center;
		margin-bottom: 20upx;
	}		
	
	.inputLabel {
		width: 150upx;
		font-size: 36upx;
		color: #8f8f94;
	}
	
	input{
		color: $uni-text-color;
		border: solid 1upx #C8C7CC;
		padding: 10upx;
		width: 400upx;
	}
</style>
