<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Novice/>
        <Borrow/>
        <Money/>
        <Product/>
        <Services/>
        <Footers/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import Footers from '../public/footer.vue'
import Navbar from '../public/navbar.vue'
import Slider from './hslide.vue'
import Novice from './novice.vue'
import Borrow from './borrow.vue'
import Money from './money.vue'
import Product from './product.vue'
import Services from './services.vue'
export default {
	components:{
		Heador,
		Slider,
		Novice,
		Borrow,
		Money,
		Product,
		Services,
		Footers,
		Navbar
	}
}
</script>


