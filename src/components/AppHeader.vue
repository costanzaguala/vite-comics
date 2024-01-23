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

    <header class="header-top">
        
    </header>

	<header class="header-bottom display-flex">
        
		<div id="logo">
			<img src="../assets/img/dc-logo.png" alt="logo-dc">
		</div>

		<nav>
			<ul class="display-flex">
				<li v-for="(elem,i) in navigationBar">
					{{ elem }}
				</li>
			</ul>
		</nav>

    </header>

</template>

<style lang="scss" scoped>

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
.display-flex {
    flex-wrap: wrap;
	display: flex;
    align-items: center;
}

ul {
	list-style: none;
}

li {
	margin: auto 10px;
}
.h2 {
    font-weight: bold;
}

</style>
