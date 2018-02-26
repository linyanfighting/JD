<template>
	<Panel title="In货推荐" :class="$style.panel">
		<section :class="$style.content">
			<div :class="$style.item" v-for="item in items" :key="item.catory">
				<img :src="item.catory" alt="">
				<section :class="$style.list">
					<div :class="$style.product" v-for="product in item.list">
						<img :src="product.img" alt="">
						<p :class="$style.title">{{product.title}}</p>
						<p :class="$style.price"><em>{{product.price}}</em>起</p>
						<article>
							<div :class="$style.wrapper">
								<div :class="$style.inner" :style="{width:product.progress+'%'}"></div>
							</div>
							<p>{{product.progress}}%</p>
						</article>
						<label v-if="product.label">{{product.label}}</label>
					</div>
					
				</section>
			</div>
		</section>
	</Panel>
</template>
<script>
	import Panel from "../core/panel.vue";
	export default{
		components:{
			Panel,
		},
		data(){
			return {
				items:[{
					catory:'//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200',
					list:[{
						img:'//img30.360buyimg.com/cf/s250x250_jfs/t15595/15/2136732080/41551/b26c2916/5a7c54cdN4ad03299.jpg',
						title:'电动牙刷',
						price:'79.00',
						progress:39,
						label:'精选'
					},{
						img:'//img30.360buyimg.com/cf/s250x250_jfs/t16168/161/1968909024/148686/2a85179/5a7be4bdN01533e62.jpg',
						title:'胶囊咖啡机',
						price:'11.00',
						progress:39,
						
					}]
				},{
					catory:'//img12.360buyimg.com/jrpmobile/jfs/t3739/82/2244582797/54399/746c7d79/5846a953N66b67d05.png?width=750&height=200',
					list:[{
						img:'//img30.360buyimg.com/cf/s250x250_jfs/t13834/192/2625202072/70435/e5b85a62/5a460eefN94289190.jpg',
						title:'智能后视镜',
						price:'90.00',
						progress:40,
					},{
						img:'//img30.360buyimg.com/cf/s250x250_jfs/t5827/255/6140287884/111611/498f9693/59683808N9253369f.jpg',
						title:'GPD口袋电脑',
						price:'75.00',
						progress:60,
					}]
				},{
					catory:'//img12.360buyimg.com/jrpmobile/jfs/t3214/113/4408032436/61548/ce316eef/5846d310Ne93f00c9.png?width=750&height=200',
					list:[{
						img:'//img30.360buyimg.com/cf/s250x250_jfs/t19087/67/359234055/152112/75036460/5a6ecc5fN565775cd.jpg',
						title:'层层轻薄雪花酥',
						price:'29.00',
						progress:39,
					},{
						img:'//img30.360buyimg.com/cf/s250x250_jfs/t14506/168/2096353267/153845/5bb0a2e6/5a6e9518N15da6f7c.jpg',
						title:'华礼脸茶',
						price:'29.00',
						progress:39,
					}]
				}]
			}
		}
		
	}
</script>


<style lang="scss" module>
	@import "../../css/element.scss";
	.panel{
		@include panel;
		.content{
			@include flex;
			.item{
				margin-bottom: 40px;
				>img{
					display: block;
					width:100%;
					height:170px;
				}
				.list{
					@include flex(row);
					.product{
						width:290px;
						margin-left:20px;
						height:396px;
						box-sizing:border-box;
						text-align: center;
						background:rgba(0,0,0,.02);
						position: relative;
						>img{
							width:180px;
							height:180px;
							margin:44px auto 20px;
						}
						.title{
							font-family: PingFangSC-Medium;
							font-size:28px;
							color:#444;
							font-weight:700;
						}
						.price{
							font-family: PingFangSC-Medium;
							font-size:20px;
							color:#999;
							
							em{
								color:#ff3232;
								font-size:36px;
								margin-right:8px;
								line-height: 1.4;
								&:before{
									content:"￥";
									font-size:28px;
								}
							}
						}
						article{
							@include flex(row);
							align-items:center;
							justify-content:space-around;
							padding:0 20px;
							height:30px;
							line-height: 30px;
							margin-top:6px;
							.wrapper{
								width:144px;
								height:10px;
								background:#f6e6e6;
								border-radius: 22px;
								.inner{
									width:40%;
									max-width: 100%;
									height:10px;
									background-image:linear-gradient(270deg,#f55 1%,#ff9c31 100%);
									border-radius: 22px;
								}
							}
							p{
								font-size: 22px;
								color:#999;
							}
						}
						label{
							position: absolute;
							left:0;
							top:0;
							font-family: PingFangSC-Medium;
							font-size:20px;
							color:#ff0000;
							padding:4px 8px;
							background-image: linear-gradient(-35deg,#c1c1c1 0,#Acacac 100%)
						}
					}
				}
			}
		}
	}
	
</style>