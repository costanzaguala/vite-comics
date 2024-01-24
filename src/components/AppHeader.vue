<script>
export default {
    data() {
        return {
            navigationBar:[
				"CHARACTERS",
				"COMICS",
				"MOVIES",
				"TV",
				"GAMES",
				"COLLECTIBLES",
				"VIDEOS",
				"FANS",
				"NEWS",
				"SHOP"
			]
             
        };
     },
    methods: {

    }
}
</script>

<template> 

    <section class="header-top">
        
    </section>

	<header class="header-bottom display-flex">
        
		<div id="logo">
			<img src="../assets/img/dc-logo.png" alt="logo-dc">
		</div>

        <nav>
            <ul class="display-flex">
                <li v-for="(elem,i) in navigationBar" :key="i">
                    <a href="">
                        {{ elem }}
                    </a>
                </li>
            </ul>
		</nav>

    </header>

</template>

<style lang="scss" scoped>

@use"../assets/scss/main.scss" as *;


nav {
    width: 60%;
    font-size: 12px;
    a {
        padding: 0px;
        font-weight: 600;
    }
}

.header-top {
    padding: 50px 0;
    background-color: var(--black);
}

.header-bottom {
    background-color: var(--white);
	width: 1200px;
	margin: 0 auto;
	justify-content: space-between;
    padding: 20px 0;

}

</style>
