<!-- src/lib/components/Pagination.svelte -->
<script lang="ts">
	export let meta_links: MetaLink[] = [];
	export let link_first: string | null = '';
	export let link_last: string | null = '';
	export let changePage: (url: string) => void;

	interface MetaLink {
		url: string | null;
		label: string;
		active: boolean;
	}
</script>

<div class="mt-8 flex items-center justify-center">
	{#if link_first}
		<button
			class="inline-flex h-[40px] min-w-[40px] items-center justify-center rounded-s-lg border border-gray-100 p-2 text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
			on:click={() => changePage(String(link_first))}
		>
			First
		</button>
	{/if}

	{#each meta_links as link}
		{#if link.url}
			<button
				class="inline-flex h-[40px] min-w-[40px] items-center justify-center border border-gray-100 p-2 text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
				class:text-white={link.active}
				class:bg-sky-500={link.active}
				on:click={() => changePage(String(link.url))}
			>
				{@html link.label}
			</button>
		{:else}
			<span class="px-4 py-2 text-gray-500">...</span>
		{/if}
	{/each}

	{#if link_last}
		<button
			class="inline-flex h-[40px] min-w-[40px] items-center justify-center rounded-e-lg border border-gray-100 p-2 text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
			on:click={() => changePage(String(link_last))}
		>
			Last
		</button>
	{/if}
</div>
