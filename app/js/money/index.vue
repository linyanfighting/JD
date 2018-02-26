<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Ada/>
        <Money/>
        <Adb/>
        <Finance/>
        <Adc/>
        <Footers cname="mfooter"/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import Footers from '../public/footer.vue'
import Navbar from '../public/navbar.vue'
import Slider from './mslide.vue'
import Ada from './ada.vue'
import Money from './money.vue'
import Adb from './adb.vue'
import Finance from './finance.vue'
import Adc from './adc.vue'

export default {
	components:{
		Heador,
		Slider,
		Ada,
		Money,
		Adb,
		Finance,
		Adc,
		Footers,
		Navbar
	}
}
</script>

<style lang="scss">
	.mfooter{
		ul{
			li:first-child{
				display:none;
			}
		}
	}
</style>


