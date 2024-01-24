<script>
export default{
	data() {
		return{
			
		};
	},
	props:{
		product:Object,
	},
	components:{
		
	},
	methods:{

	}
}

</script>

<template>
	<div>
		<div class="card-product">
			<div class="img-container">
				<img :src="product.thumb" :alt="product.series">
			</div>
			<h3 class="white-text">
				{{ product.series }}
			</h3>
		</div>
	</div>
</template>

<style lang ="scss" scoped>
@use"../assets/scss/main.scss" as *;


h3 {
	margin: 20px 0;
	font-size: 12px;
	text-transform: uppercase;
	font-weight: 400;

}

.img-container {
	max-width: 150px;
	height: 150px;
}

img {
    width: 100%;
	height: 100%;
}
</style>