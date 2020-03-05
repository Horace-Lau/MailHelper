<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<view class="text-input">
				<text class="title">用户名：</text>
				<input id="username" type="text" name="username" placeholder="用户名/手机号"/>
			</view>
			<view class="text-input">
				<text class="title">密码：</text>
				<input id="password" type="text" name="password" password="true" placeholder="密码"/>
			</view>
			<inputNormal inputLabel="测试1" phHolder="ph1"></inputNormal>
			<button  class="loginBtn" size="mini" @click="login">登录</button>
		</view>
	</view>
</template>

<script>
	import inputNormal from '@/components/form/input-normal';
	export default {
		components:{
				inputNormal
			},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			login(){
				console.log('登录中...')
				uni.redirectTo({
					url:'../mailSetting/mailsetting'
				})
			}
		}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		align-items: center;
		flex-wrap: wrap;
	}
	
	.text-input{
		width: 100%;
		display: flex;
		flex-wrap: nowrap;
		justify-content: center;
		align-items: center;
		margin-bottom: 20upx;
	}		

	.title {
		width: 150upx;
		font-size: 36upx;
		color: #8f8f94;
	}
	
	#username,#password{
		color: $uni-text-color;
		border: solid 1upx #C8C7CC;
		padding: 10upx;
		width: 400upx;
	}
	
	.loginBtn{
		color: #fff;
		background-color: #007AFF;
	}
</style>
