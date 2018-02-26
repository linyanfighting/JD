<template lang="html">
	<article>
		<Slider :items="items" :cname="$style.slider"/>
		<section :class="$style.list">
			<div :class="$style.item" v-for="item in enters" :key="item.img">
				<router-link :to="{name:item.href}">
					<img :src="item.img" :alt="item.title" />
					<h4>{{item.title}}</h4>
				</router-link>
			</div>
		</section>
	</article>
</template>

<script>
import Slider from "../core/slider.vue"
	export default{
		components:{
			Slider
		},
		data(){
			return {
				items: [{
					href:'home',
					src:"//img12.360buyimg.com/jrpmobile/jfs/t19591/154/491844579/36367/71fc5822/5a8e7f85Nf86bad30.jpg?width=750&height=320",
				},{
					href:'home',
					src:"//img12.360buyimg.com/jrpmobile/jfs/t18709/24/500005431/45321/16a8511d/5a8e7fa8N358d2fa9.jpg?width=750&height=320",
				},{
					href:'home',
					src:"//img12.360buyimg.com/jrpmobile/jfs/t15769/324/2117947588/43865/7100cb97/5a8e7fc6N75b6faf5.jpg?width=750&height=320",
				},{
					href:'home',
					src:"//img12.360buyimg.com/jrpmobile/jfs/t19318/85/490045627/49917/e5ad6c1/5a8e7fe2N5c2945c6.jpg?width=750&height=320",
				}],
				enters:[{
					href:'download',
					img:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
					title:'优惠券'
				},{
					href:'home',
					img:"//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
					title:'领红包'
				},{
					href:'home',
					img:"//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
					title:'抢钢镚'
				},{
					href:'home',
					img:"//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
					title:'白额提条'
				}]
			}
		}
	}
</script>

<style lang="scss" module>
	@import "../../css/element.scss";
	.slider{
		margin-top:100px;
		img{
			width:100%;
		}
		a{
			margin:0;
		}
	}
	.list{
		@include list(row);
		background:#fff;
		padding-top:30px;
		padding-bottom:20px;
		justify-content:space-around;
		a{
			text-decoration: none;
			margin:0;
		}
		.item{
			text-align: center;
			img{
				display: inline-block;
				width:80px;
				height:80px;
			}
			h4{
				font-size:22px;
				margin-top:10px;
				color:#666;
			}
		}
	}
</style>