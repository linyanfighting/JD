<template>
	<Panel title="更多服务" :class="$style.panel">
		<section :class="$style.content">
			<ul>
				<li v-for="item in items">
					<img :src="item.src" alt="">
					<p>{{item.title}}</p>
				</li>
			</ul>
		</section>
	</Panel>
</template>

<script>
	import Panel from "../core/panel";
	export default{
		components:{
			Panel
		},
		data(){
			return {
				items:[{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t4609/245/3975151339/11019/766e751d/590aca78Nf15a7947.png?width=135&height=135",
					title:"小白卡"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t5269/224/1031852465/12646/40e0f799/590aca55N22a6f274.png?width=135&height=135",
					title:"白条商城"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t5095/216/1045040184/12370/564ae632/590ac7deN9a0eac2a.png?width=135&height=135",
					title:"消费分期"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t8311/300/1385281399/9501/130a0046/59b8da06N14f62cf3.png?width=120&height=120",
					title:"借钱"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
					title:"白条提款"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
					title:"白条闪付"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
					title:"小白会玩"
				},{
					src:"//img12.360buyimg.com/jrpmobile/jfs/t5371/323/1038197138/12031/3ec72f6c/590aca20N089fd34a.png?width=135&height=135",
					title:"钢镚"
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
			padding-bottom:10px;
			ul{
				@include flex(row);
				li{
					width:25%;
					text-align: center;
					margin-bottom:30px;
					img{
						width:80px;
						height:80px;
					}
					p{
						color:#666;
						font-size:24px;
						line-height: 1.8;
					}
				}
			}
		}
	}
</style>