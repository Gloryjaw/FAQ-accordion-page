<script>
import Faq from "./components/Faq.svelte";
import HeroImg from "./components/Hero-img.svelte";

</script>

<main>
	<HeroImg/>
	<Faq/>

</main>

<style>

	main{
		background-color: white;
		position: relative;
		padding: 0 1.5em ;
		border-radius: 25px;
		padding-bottom: 2.8em;
		width: 85%;
		max-width: 350px;
	}
	@media (min-width: 1050px){
		main{
			width: 60%;
			display: flex;
			max-width: none;
			padding: 4em 0;
			background-image: url(../images/bg-pattern-desktop.svg);
			background-size: 96%;
    	background-repeat: no-repeat;
    	background-position: -1342% 64%;

		}
	}
</style>
