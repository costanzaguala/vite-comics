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

    <section class="section-large">
        
    </section>

	<section class="section-medium display-flex">
        
		<div id="logo">
			<img src="../assets/img/dc-logo.png" alt="">
		</div>

		<nav>
			<ul class="display-flex">
				<li v-for="(elem,i) in navigationBar">
					{{ elem }}
				</li>
			</ul>
		</nav>

    </section>

    <section class="section-large">

        <div class="section-medium">
            <h2>
        --> Content goes here <--
            </h2>
        </div>
        
    </section>

    <section class="section-large">

<div class="section-medium">
    <h2>
--> Content goes here <--
    </h2>
</div>

</section>


        
</template>

<style lang="scss" scoped>

.section-large {
    background-color: black;
    padding: 50px 0;
    color: white;
}

.section-medium {
	width:1200px;
	margin:0 auto;
	justify-content: space-between;
    padding: 20px 0;

}
.display-flex {
    flex-wrap: wrap;
	display:flex;
    align-items: center;
}

ul {
	list-style: none;
}

li {
	margin:auto 10px;
}
.h2 {
    font-weight: bold;
}

</style>
