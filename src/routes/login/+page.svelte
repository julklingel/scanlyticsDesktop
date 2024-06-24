<script lang="ts">
    import { enhance } from '$app/forms';
    import Card from '../components/ui/Card.svelte';
	import GlowyBalls from '../components/ui/GlowyBalls.svelte';
    import IconHouse from '@iconify/svelte';
    import { goto } from '$app/navigation';

	import { focusTrap } from '@skeletonlabs/skeleton';
	let isFocused: boolean = true;
</script>

<GlowyBalls />

<div class="h-screen z-10 w-screen flex justify-center shadow-2xl items-center">
	<Card>
        <div class="flex justify-center items-center mb-4">
            <button on:click={() => goto('./')}>
            <IconHouse icon="line-md:home-twotone-alt" class="text-4xl" />
        </button>
        </div>
		<form method="POST" action="/login" use:enhance class="flex flex-col gap-4 " use:focusTrap={isFocused}>
			<input type="email" placeholder="Email" class="p-2 dark:bg-surface-700 border rounded-3xl" />
			<input type="password" placeholder="Password" class="p-2 dark:bg-surface-700 bg-surface border rounded-3xl" />
			<button type="submit" class="btn variant-filled-primary hover:variant-filled-secondary shadow-3xl">
				<span class="font-bold text-white">Login </span>
			</button>
		</form>
	</Card>
</div>
