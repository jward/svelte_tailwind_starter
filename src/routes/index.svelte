<script lang="ts">
	import { fade, scale } from 'svelte/transition';
	import { currentUser } from '../stores/user-stores';
	import LoginButton from '../components/login-button.svelte';

	import User from '../components/user.svelte';
</script>

<div class="p-4">
	<h1 class="text-4xl mb-8">Welcome to SvelteKit</h1>

	<LoginButton />

	{#if $currentUser}
		<div in:scale out:fade={{ duration: 100 }}>
			<User user={$currentUser} />
		</div>
	{/if}
</div>

<style>
</style>
