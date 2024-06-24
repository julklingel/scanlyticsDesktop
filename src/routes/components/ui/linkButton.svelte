<script>
	export let link 
	export let buttonText
	import { goto } from '$app/navigation';
</script>

<button
	class="btn variant-filled-primary hover:variant-filled-secondary"
	on:click={() => goto(link)}
>
	<span class="font-bold text-white">{buttonText}</span>
	<span class="btn-fill"></span>
</button>

<style lang="postcss">
	.btn {
		position: relative;
		display: inline-flex;
		align-items: center;
		justify-content: center;
		padding: 0.75rem 1.5rem;
		overflow: hidden;
		font-medium: bold;
		transition: all 0.3s;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
	}

	.btn-fill {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		transition: all 0.3s ease-out;
		transform: translateX(100%);
	}

	.btn::before {
		content: '';
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		transition: all 0.3s ease-out;
		transform: translateX(0);
	}

	.btn:hover .btn-fill {
		transform: translateX(0);
	}

	.btn:hover::before {
		transform: translateX(-100%);
	}

	.btn:hover {
		transform: scale(1.05);
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
	}
</style>
