<script>
</script>

<section class=" absolute -z-10">

<div class="glowy-balls fixed right-1/2 bottom-1/2"></div>
<div class="glowy-balls fixed left-1/2 top-1/2"></div>
</section>

<style lang="postcss">
	.glowy-balls {
		@apply w-96 h-96 rounded-full blur-[80px] transition-all;
		animation:
			pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite,
			glow 5s linear infinite;
	}

	@keyframes glow {
		0% {
			@apply bg-primary-400/50;
		}
		33% {
			@apply bg-secondary-400/50;
		}
		66% {
			@apply bg-tertiary-400/50;
		}
		100% {
			@apply bg-primary-400/50;
		}
	}

	@keyframes pulse {
		50% {
			transform: scale(2);
		}
	}

	
</style>

