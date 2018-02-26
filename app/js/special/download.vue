<template>
	<Panel title="下载APP" :class="$style.panel">
		<section :class="$style.content">
			<div></div>
			<p>立即下载</p>
			<span>已安装，点击这里直接打开</span>
		</section>
	</Panel>
</template>
<script>
	import Panel from "../core/panel.vue"
	export default{
		components:{
			Panel
		}
	}
</script>
<style lang="scss" module>
	@import "../../css/element.scss";
	
	html body{
		background: #fff;
	}
	.panel{
		@include panel;
		margin:0!important;
		>h4{
			display: none;
		}
		.content{
			@include flex;
			justify-content:center;
			align-items:center;
			height:1136px;
			width:100%;
			>div{
				background: url(https://img12.360buyimg.com/jrpmobile/jfs/t10054/120/2165982932/56512/574e4766/59f031f3N1a75e42d.png?width=1125&height=890)center center no-repeat;
				width:600px;
				height:800px;
				background-size: 100% auto;
			}
			p{
				@include btn($size:32px,$color:#fff,$bgcolor:#f1443E,$padding:5px,$radius:5px);
				height:80px;
				line-height: 80px;
				width:451px;
				text-align:center;
				background-image:linear-gradient(270deg,#f55c33 0,#ee2d1b 75%);
				box-shadow: 0 12px 32px 0 rgba(255,159,135,.6);
				position: fixed;
				bottom:100px;
			}
			span{
				position: fixed;
				bottom:40px;
				font-size:24px;
				color:#F4552F;
			}

		}
	}
</style>
