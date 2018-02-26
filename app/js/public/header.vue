<template lang="html">
	<div :class="$style.header">
		<span :class="$style.left">
			<em>注册</em> | <em>登录</em>
		</span>
		<btn :class="$style.btnDownload">APP下载</btn>
	</div>
</template>

<script>
	import btn from '../core/btn.vue'
	export default{
		components: {
			btn
		}
	}
</script>

<style lang="scss" module>
	.header{
		color:#666;
		height:80px;
		line-height: 80px;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		font-size: 32px;
		background: #f9f9f9 url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png)no-repeat center center;
		background-size:auto 60%;
		z-index:100;
		.left{
			font-size:24px;
			height:30px;
			line-height:30px;
			margin: 17px 0 0 18px;
		}
		.btnDownload{
			float:right;
			font-size:20px;
			min-width:100px;
			height:48px;
			line-height:48px;
			border-radius: 4px;
			margin: 20px 22px 0 0;
			padding:0;

		}
	}

</style>