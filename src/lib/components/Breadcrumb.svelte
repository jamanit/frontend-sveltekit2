<script lang="ts">
	export let breadcrumbTitle: string = '';
	[];
	export let breadcrumbItems: { name: string; url: string; isActive?: boolean }[] = [];

	const baseURL = import.meta.env.VITE_BASE_URL;
</script>

<nav class="bg-gray-500 py-[37px]"></nav>
<section
	class="relative table w-full bg-[url({`${baseURL}/assets/hoxia-v1/images/bg/bg5.png`})] bg-cover bg-center py-36 md:py-40"
>
	<div class="absolute inset-0 bg-sky-500/5"></div>
	<div class="relative container">
		<div class="mt-12 grid grid-cols-1 text-center">
			<h3 class="text-3xl leading-snug font-medium md:text-4xl md:leading-snug">
				{breadcrumbTitle}
			</h3>
		</div>
	</div>

	<div class="absolute start-0 end-0 bottom-5 z-10 mx-3 text-center">
		<ul class="mb-0 inline-block tracking-[0.5px]">
			{#each breadcrumbItems as { name, url, isActive }, index}
				{#if index === 0}
					{#if isActive}
						<li class="inline-block text-[15px] font-medium text-sky-500 duration-500 ease-in-out">
							{name}
						</li>
					{:else}
						<li
							class="inline-block text-[15px] font-medium duration-500 ease-in-out hover:text-sky-500"
						>
							<a href={url} data-sveltekit-prefetch>{name}</a>
						</li>
					{/if}
				{/if}

				{#if index !== 0}
					<li class="inline-block text-[15px] ltr:rotate-0 rtl:rotate-180">
						<i class="mdi mdi-chevron-right"></i>
					</li>

					{#if isActive}
						<li class="inline-block text-[15px] font-medium text-sky-500 duration-500 ease-in-out">
							{name}
						</li>
					{:else}
						<li
							class="inline-block text-[15px] font-medium duration-500 ease-in-out hover:text-sky-500"
						>
							<a href={url} data-sveltekit-prefetch>{name}</a>
						</li>
					{/if}
				{/if}
			{/each}
		</ul>
	</div>
</section>

<div class="relative">
	<div
		class="shape absolute start-0 end-0 -bottom-[2px] z-1 overflow-hidden text-white sm:-bottom-px dark:text-slate-900"
	>
		<svg class="h-auto w-full" viewBox="0 0 2880 48" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path d="M0 48H1437.5H2880V0H2160C1442.5 52 720 0 720 0H0V48Z" fill="currentColor"></path>
		</svg>
	</div>
</div>
