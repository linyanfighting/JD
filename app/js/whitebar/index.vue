<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Welfare/>
        <Service/>
        <Footers/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import Footers from '../public/footer.vue'
import Navbar from '../public/navbar.vue'
import Slider from './wslide.vue'
import Welfare from './welfare.vue'
import Service from './service.vue'


export default {
	components:{
		Heador,
		Slider,
		Welfare,
		Service,
		Footers,
		Navbar
	}
}
</script>



