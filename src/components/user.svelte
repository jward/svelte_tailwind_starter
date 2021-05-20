<script lang="ts">
	import type { User } from '../types';
	export let user: User;
</script>

<div class="mb-4">
	<h1 class="font-thin text-2xl py-2">{user.name}</h1>
	My age is <b>{user.age}</b>
</div>
