<script>
	import AboutComponent from './components/AboutComponent.svelte';
	import TextComponent from './components/TextComponent.svelte';
	import PersonComponent from './components/PersonComponent.svelte';
	import SkillsComponent from './components/SkillsComponent.svelte';
	import InputComponent from './components/InputComponent.svelte';
	import ImagesComponent from './components/ImagesComponent.svelte';
	import ButtonComponent from './components/ButtonCount.svelte';
import ButtonCount from './components/ButtonCount.svelte';


	export let name;
	export let lastName;
	
	let svelteLogo = ' https://arepa.s3.amazonaws.com/svelte-logo.png';

	const data = {
		name: 'Andres',
		lastName: 'Pardo',
		age: 32
	}

</script>

<style>

	/*Aplicar estilos globales al body f2eee2*/
	:global(body){
		background-color: #f2eee2;
		color: #0084f6;
	}

	/*variables globales al documento*/
	:global(:root){
		/*--theme-color: purple,*/
		--color-darkMode: #bfc2c7,
	}

	:global(body.dark-mode){
		background-color: #1d3040;
		color: #bfc2c7;
	}

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	main img {
		width: 30%;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Hello {name} {lastName} !</h1>
	<AboutComponent/>
	<TextComponent anotherText='Locos'/>
	<TextComponent />
	<PersonComponent data={data}/>
	<SkillsComponent />
	<InputComponent />
	<ButtonCount />	
	<ImagesComponent/>
	<img src={svelteLogo} alt={'Logo'}/>
</main>

