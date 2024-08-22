<script lang="ts">
	import TimeClock from '$lib/TimeClock.svelte';
	import '$lib/styles.css';

</script>
<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" style="text-decoration: none; color: inherit;">
	<header>
		<h1>BreatheBox</h1>
		<TimeClock />
	</header>
</a>


<main class="container" style="display: grid;">
	<!-- {#if $clerk_store?.user || anon} -->
	<slot />
	<!-- {:else}
		<h2>Welcome, are you ready to breathe?</h2>
		<p>Create an account to track, or anonymous just to try.</p>

		<button
			on:click={() => {
				signin = true;
			}}>Login</button
		>
		<button
			on:click={() => {
				signup = true;
			}}>Sign Up</button
		>
		<p>or</p>
		<button
			on:click={() => {
				anon = true;
			}}>Anonymous</button
		>
	{/if}
	{#if signin || signup}
		<div class="overlay">
			<button
				on:click={() => {
					signin = false;
					signup = false;
				}}>Close</button
			>
			{#if signin}
				<Signin />
			{/if}
			{#if signup}
				<Signup />
			{/if}
		</div>
	{/if} -->
</main>

<footer>
	<!-- <button class="subtle" on:click={refresh_devices}>↻ | Refresh Devices</button> -->
	<h3>Helpful Links</h3>
	<ul>
		<li>
			<a
				href="https://learningevaluationcenter.org/box-breathing-a-mindfulness-technique-for-parents-of-teens-with-anxiety/"
				>What is box breathing?</a
			>
		</li>
		<li>
			<a href="https://www.webmd.com/balance/what-is-box-breathing"
				>How Box Breathing Helps</a
			>
		</li>
		<li><a href="https://www.instagram.com/naval_shah_29/">Secret Link</a></li>
	</ul>
</footer>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	h1 {
		margin-top: 0;
		text-shadow: 1px 1px 0 oklch(60% 0.229 262.97);
		transition: 2s ease-in-out text-shadow;
		font-weight: 100;
		font-style: italic;
	}
	h1:hover {
		text-shadow: 10px 10px 4px oklch(60% 0.229 262.97);
	}
	.container {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 20px;
		max-width: 600px;
		align-self: center;
	}

	.overlay {
		position: fixed;
		inset: 100px 0;
	}

	:global(.cl-rootBox) {
		margin: 0 auto;
	}
</style>
