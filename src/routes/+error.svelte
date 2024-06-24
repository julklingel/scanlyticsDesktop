<script lang="ts">
	import Card from './components/ui/Card.svelte';
	import IconError from '@iconify/svelte';
	import IconBack from '@iconify/svelte';
	import { page } from '$app/stores';
	import { goto } from '$app/navigation';

	let link = './login';
</script>

<section class="h-screen z-10 w-screen flex justify-center shadow-2xl items-center">
	<Card>
		<div class="flex justify-between">
			<h1 class="h1 pb-4">Uups...</h1>
			<IconError class="h1 text-warning-500" icon="line-md:alert-circle-loop" />
		</div>

		<h3 class="h3 w-full">{$page.status}: {$page.error?.message}</h3>

		<div class=" justify-center items-center pt-4">
			<button class="btn bg-primary-500 hover:bg-secondary-500" on:click={() => goto('./')}>
				<IconBack icon="ep:back" class="text-3xl text-white" />
				<span class="font-bold text-white">Back</span>
			</button>
		</div>
	</Card>
</section>
