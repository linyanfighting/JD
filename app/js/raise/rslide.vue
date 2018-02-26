<template>
	<Panel title="金融头条" :class="$style.panel">
		<section :class="$style.content">
			<swiper :options="options">
				<swiper-slide>签到领流量，1元500M！ <em>></em></swiper-slide>
				<swiper-slide>百万白条券免费送，速来领取！！<em>></em></swiper-slide>
			</swiper>
		</section>
	</Panel>
</template>
<script>
	import Panel from "../core/panel.vue";
	import {swiper,swiperSlide} from 'vue-awesome-swiper'
	export default{
		components:{
			Panel,
			swiper,
			swiperSlide
		},
		data(){
			return {
				options:{
					autoplay: true,
					loop: true,
					direction:"vertical"
				}
			}
		}
	}
</script>

<style lang="scss">
	.swiper-container-vertical{
		height:72px;
		.swiper-slide{
			font-size:24px;
			color:#333;
			font-family: PingFangSC-Medium;
			em{
				float: right;
				font-size:30px;
				color:#ddd;
				margin-right:20px;
			}
		}
	}

</style>
<style lang="scss" module>
	@import "../../css/element.scss";
	.panel{
		@include panel;
		margin-bottom:0!important;
		>h4{
			display: none;
		}
		.content{
			margin-top:100px;
			height:72px;
			line-height: 72px;
			overflow: hidden;
			padding-left: 166px;
			background:url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png)left center no-repeat;
		}
	}
	
</style>