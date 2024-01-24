<script>

import AppProductCard from './AppProductCard.vue'
import AppBlueBar from './AppBlueBar.vue';


export default{
	data() {
		return{
			products:[
				{
					"thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
					"price": "$19.99",
					"series": "Action Comics",
					"type": "comic book",
				},
				{
					"thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
					"price": "$3.99",
					"series": "American Vampire 1976",
					"type": "comic book",
				},
				{
					"thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
					"price": "$16.99",
					"series": "Aquaman",
					"type": "graphic novel",
				},
				{
					"thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
					"price": "$2.99",
					"series": "Batgirl",
					"type": "comic book",
				},
				{
					"thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
					"price": "$3.99",
					"series": "Batman",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
					"price": "$2.99",
					"series": "Batman Beyond",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
					"price": "$3.99",
					"series": "Batman/Superman",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
					"price": "$4.99",
					"series": "Batman/Superman Annual",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
					"price": "$5.99",
					"series": "Batman: The Joker War Zone",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
					"price": "$6.99",
					"series": "Batman: Three Jokers",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
					"price": "$4.99",
					"series": "Batman: White Knight Presents: Harley Quinn",
					"type": "comic book",
				},
				{
					"thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
					"price": "$16.99",
					"series": "Catwoman",
					"type": "graphic novel",
				},
			]
		};
	},
	components:{
    AppProductCard,
    AppBlueBar,
},
	methods:{
		getImagePath(imgPath){
			return new URL (imgPath, import.meta.url).href;
		}
	}
}

</script>

<template>
	<main>
		<div class="container">
			<div id="current-series" class="white-text">
				Current Series
			</div>
			<div class="products-container display-flex">
                <AppProductCard Product class="col-1-6" v-for="(elem, i) in products" :key="i" :product="elem"/>
            </div>

            <div class="display-flex justify-content-center">
                <button class="white-text">
			        LOAD MORE
		        </button>
            </div>
		</div>
	</main>

    <AppBlueBar/>
</template>


<style lang="scss" scoped>

@use"../assets/scss/main.scss" as *;

main {
    padding: 30px 0 ;
    background-color: var(--grey);
}

.container {
    position: relative;
}

.products-container {
    padding: 30px 0;
}
.col-1-6 {
	width: calc(100% / 6);
    padding: 0 25px;
}

#current-series {
    padding: 10px;
    background-color: var(--blue);
    width: 160px;
    font-size: 15px;
    position:absolute;
    bottom: 100%;
    left: 0;
    text-align: center;
    font-weight: 800;
    text-transform: uppercase;
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

button {
    padding: 10px 20px;
    font-weight: bold;
    font-size: 15px;
    border: none;
    background-color: var(--blue);
}

button:hover {
        color: var(--grey);
  
}
</style>