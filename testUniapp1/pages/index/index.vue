<template>
	<view class="content">
		<view class="form-container">
			<image class="logo" src="/static/orange-logo.png"></image>
			<view v-if="isLogin">
				<h2>登录小橘子</h2>
				<input v-model="loginForm.username" placeholder="用户名/手机号" />
				<input v-model="loginForm.password" type="password" placeholder="密码" />
				<button @click="handleLogin">登录</button>
				<view class="action-links">
					<text @click="toggleForm">注册账号</text>
					<text>忘记密码</text>
				</view>
			</view>
			<view v-else>
				<h2>注册小橘子</h2>
				<input v-model="registerForm.username" placeholder="用户名/手机号" />
				<input v-model="registerForm.password" type="password" placeholder="密码" />
				<input v-model="registerForm.confirmPassword" type="password" placeholder="确认密码" />
				<button @click="handleRegister">注册</button>
				<view class="action-links">
					<text @click="toggleForm">返回登录</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isLogin: true,
				loginForm: {
					username: '',
					password: ''
				},
				registerForm: {
					username: '',
					password: '',
					confirmPassword: ''
				}
			}
		},
		methods: {
			toggleForm() {
				this.isLogin = !this.isLogin
			},
			handleLogin() {
				if (this.loginForm.username === 'root' && this.loginForm.password === 'root') {
					// 登录成功，跳转到首页
					uni.showToast({
						title: '登录成功',
						icon: 'success'
					});
					uni.navigateTo({
						url: '/pages/home/home'
					});
				} else {
					// 登录失败
					uni.showToast({
						title: '用户名或密码错误',
						icon: 'none'
					});
				}
			},
			handleRegister() {
				// 实现注册逻辑
				console.log('注册', this.registerForm)
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		min-height: 100vh;
		background-color: #FFF5E6;
	}

	.form-container {
		width: 80%;
		max-width: 300px;
		background-color: #FFFFFF;
		padding: 30px;
		border-radius: 10px;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
		text-align: center;
	}

	.logo {
		width: 80px;
		height: 80px;
		margin: 0 auto 20px;
		display: block;
	}

	h2 {
		text-align: center;
		margin-bottom: 20px;
		color: #FF6600;
		font-size: 24px;
	}

	input {
		/* width: 100%; */
		height: 40px;
		margin-bottom: 15px;
		padding: 0 15px;
		border: 1px solid #FFB366;
		border-radius: 20px;
		font-size: 14px;
		text-align: center;
	}

	button {
		width: 100%;
		height: 40px;
		background-color: #FF6600;
		color: white;
		border: none;
		border-radius: 20px;
		margin-bottom: 15px;
		font-size: 16px;
		font-weight: bold;
	}

	.action-links {
		display: flex;
		justify-content: center;
		gap: 20px;
	}

	text {
		color: #FF6600;
		font-size: 14px;
	}
</style>
