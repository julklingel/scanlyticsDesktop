<script>
  	import GlowyBalls from './components/ui/GlowyBalls.svelte';
  	import LinkButton from './components/ui/linkButton.svelte';
	export let link = './login';
	export let buttonText = 'Login';
	

</script>

<GlowyBalls/>

<div class=" h-screen w-screen mx-auto flex justify-center items-center">
	<div class="space-y-10 text-center flex flex-col items-center">
		<h2 class="h1 font-sans z-10 text-primary-500 font-bold">Scanlytics</h2>
		<div class="z-10 justify-center space-x-2">
		<LinkButton {link} {buttonText}/>
		</div>
	</div>
</div>

