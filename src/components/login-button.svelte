<script lang="ts">
	import { currentUser } from '../stores/user-stores';

	const loginUser = () =>
		($currentUser = {
			name: 'John Doe',
			age: 27
		});

	const logoutUser = () => ($currentUser = null);

	const toggleLogin = () => ($currentUser ? logoutUser() : loginUser());

	$: btnColorClass = $currentUser ? 'bg-red-400' : 'bg-blue-400';
</script>

<button
	class="{btnColorClass} focus:outline-none rounded-full border-none outline-none p-4 text-white"
	on:click={toggleLogin}
>
	{$currentUser ? 'Log Out' : 'Login'}
</button>
