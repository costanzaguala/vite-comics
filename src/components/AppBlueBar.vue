<script>

export default{
	data() {
		return{
            navigationBar:[

				{
					name:"DIGITAL COMICS",
					path:"../assets/img/buy-comics-digital-comics.png"
				},
				{
					name:"DC MERCHANDISE",
					path:"../assets/img/buy-comics-merchandise.png"
				},
				{
					name:"SUBSCRIPTION",
					path:"../assets/img/buy-comics-subscriptions.png"
				},
				{
					name:"COMICS SHOP LOCATOR",
					path:"../assets/img/buy-comics-shop-locator.png"
				},
				{
					name:"DC POWE VISA",
					path:"../assets/img/buy-dc-power-visa.svg"
				}
				
			]
		};
	},
	components:{
	
	},
	methods:{
		getImagePath(imgPath){
			return new URL (imgPath, import.meta.url).href;
		}
	}
}

</script>

<template>
    <section>

        <div class="blue-background">
            <div class="container">
                <ul class="display-flex justify-content-space-between">
                    <li v-for="(elem) in navigationBar" class="display-flex">
                        <div class="img-container">
                            <img :src="getImagePath(elem.path)"  alt="">
                        </div>
                        <a href="" class="white-text">
                            {{ elem.name }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
		
    </section>
</template>

<style lang="scss" scoped>

@use"../assets/scss/main.scss" as *;

.blue-background {
    background-color: var(--blue);
    padding: 60px 0;
}

.img-container {
	max-width: 50px;
	height: 50px;
}

img {
    width: 100%;
	height: 100%;
}

a {
    font-size: 12px;
}
</style>