<script>
export default {
    data() {
        return {

            comicsList:[
				"Characters",
				"Comics",
				"Movies",
				"TV",
				"Games",
				"Videos",
				"News"
			],

			shopList:[
				"Shop DC",
				"Shop DC collectibles"
			],

			dcList:[
				"Terms Of Use",
				"Privacy policy(New)",
				"Ad Choices",
				"Advertising",
				"Jobs",
				"Subscriptions",
				"Talent Workshops",
				"CPSC Certificates",
				"Ratings",
				"Shop Help",
				"Concact Us"
			],
			siteList:[
				"DC",
				"MAD Magazine",
				"DC Kids",
				"DC Universe",
				"DC Power Visa"
			],

            socialIcons:[
			"footer-facebook.png",
            "footer-pinterest.png",
			"footer-twitter.png",
			"footer-youtube.png",
			"footer-periscope.png",
			],

        };

        
     },
    methods: {
        getImagePath(imgPath){
			return new URL (imgPath, import.meta.url).href;
		}
    }
}
</script>

<template>
    <footer>
        <div class="top-footer">
			<div class="container display-flex justify-content-space-between">
				<div id="left-side" class="display-flex">
					<div class="col-1">
						<div>
							<h4 class="white-text">
                                DC COMICS
                            </h4>

							<ul>
								<li v-for="(elem) in comicsList" :key="i">
									{{ elem }}
								</li>
							</ul>

							<h4 class="white-text">
                                SHOP
                            </h4>

							<ul>
								<li v-for="(elem) in shopList" :key="i">
									{{ elem }}
								</li>
							</ul>
						</div>
					</div>

                    <div class="col-1">
						<h4 class="white-text">
							DC
						</h4>

						<ul>
							<li v-for="(elem) in dcList" :key="i">
								{{elem}}
							</li>
						</ul>
					</div>

                    <div class="col-1">
						<h4 class="white-text">
							SITES
						</h4>

						<ul>
                            <li v-for="(elem,i) in siteList" :key="i">
								{{ elem }}
							</li>
						</ul>
					</div>
                </div>

                <div id="right-side">
                </div>
			</div>
        </div>

		<div class="bottom-footer">
			<div class="container">
				<div class="display-flex justify-content-space-between align-items-center">
					<button class="white-text">
						SIGN-UP NOW!
					</button>

					<div class="social display-flex">
						<div>
							FOLLOW US
						</div>
						<div class="container-social">
							<img v-for="(elem) in socialIcons" :src="getImagePath('../assets/img/'+ elem)" alt="">
						</div>
					</div>
				</div>
			</div>
		</div>

        <section class="footer-bottom-section">
        
        </section>
	</footer>

</template>

<style lang="scss" scoped>

@use"../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as *;

.grey-background {
    background-color: var(--grey);
}

.top-footer {
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    background-repeat: no-repeat;

    :first-child {
    align-items: stretch;
    }

}

ul {
    padding: 5px 0;
}

li {
    margin: 5px 0;
    color: var(--light-grey);
    font-size: 14px;
}

#left-side {
    width: 50%;
    height: 100%;
    padding: 50px 0;

}

#right-side {
    width: 40%;
    background-image: url("../assets/img/dc-logo-bg.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
 }
.col-1 {
    width: calc(100/3);
    padding: 0 20px;
}
.bottom-footer {
    height: 90px;
    vertical-align: middle;
    background-color: var(--grey);
    .container {
			height: 100%;
			> *{
				height: 100%;
			}
		}
}

button {
    padding: 10px;
    font-weight: bold;
    font-size: 16px;
    border: 2px solid var(--blue);
    background-color: transparent;
}

.social {
    & >*:first-child {
        color: var(--blue);
        line-height: 30px;
        vertical-align: middle;
        font-size: 18px;
        font-weight: bold;
        margin-right: 30px;
    }
}

 .container-social, img {
    margin-right: 15px;
}

.footer-bottom-section {
    padding: 50px 0;
    background-color: var(--black);

}
</style>