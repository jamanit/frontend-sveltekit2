<script lang="ts">
	import { onMount } from 'svelte';
	import { page } from '$app/stores';
	import Breadcrumb from '$lib/components/Breadcrumb.svelte';
	import Button from '$lib/components/Button.svelte';
	import { showToast } from '$lib/utils/toast';
	import Pagination from '$lib/components/Pagination.svelte';

	let breadcrumbTitle = 'Latest Post';
	let breadcrumbItems = [
		{ name: 'Home', url: '/' },
		{ name: 'Posts', url: '', isActive: true }
	];

	const baseURL = import.meta.env.VITE_BASE_URL;
	const apiBaseURL = import.meta.env.VITE_API_BASE_URL;

	type Post = {
		id: number;
		judul_berita: string;
		content_body: string;
		tanggal: string;
		images: string;
		images_caption: string;
		jumlah_view: number;
		status: string;
		category_id: number;
	};

	interface MetaLink {
		url: string | null;
		label: string;
		active: boolean;
	}

	let postUrl = `${apiBaseURL}/api/posts`;
	let searchParam: string | undefined = undefined;
	let posts: Post[] = [];
	let meta_links: MetaLink[] = [];
	let link_first: string | null = '';
	let link_last: string | null = '';
	let message = '';
	// let meta_total: number | null = null;
	// let meta_current_page: number | null = null;
	// let meta_per_page: number | null = null;
	// let meta_last_page: number | null = null;
	// let meta_from: number | null = null;

	async function getPosts(postUrl: String) {
		try {
			const response = await fetch(`${postUrl}`, {
				method: 'GET'
			});

			if (!response.ok) {
				throw new Error(`Failed to fetch: ${response.status}`);
			}

			const result = await response.json();
			posts = result.data;
			meta_links = result.meta.links;
			link_first = result.links.first;
			link_last = result.links.last;
			// meta_total = result.meta.total;
			// meta_current_page = result.meta.current_page;
			// meta_per_page = result.meta.per_page;
			// meta_last_page = result.meta.last_page;
			// meta_from = result.meta.from;
		} catch (err) {
			message = 'Error fetching posts.';
			console.error(err);
		}
	}

	function buildUrl(base: string, search?: string) {
		return search ? `${base}?search=${search}` : base;
	}

	onMount(() => {
		page.subscribe(($page) => {
			searchParam = $page.url.searchParams.get('search') || undefined;
			const fullUrl = buildUrl(postUrl, searchParam);
			getPosts(fullUrl);
		});
	});

	// Handle pagination and maintain search parameter
	function changePage(newUrl: string) {
		if (newUrl) {
			const paginatedUrl = buildUrl(newUrl, searchParam);
			getPosts(paginatedUrl);
		}
	}

	function highlightText(text: string, searchTerm: string | undefined) {
		if (!searchTerm || searchTerm.trim() === '') {
			return text;
		}
		const regex = new RegExp(`(${searchTerm})`, 'gi');
		return text.replace(regex, '<mark class="bg-yellow-300">$1</mark>');
	}
</script>

<div>
	<Breadcrumb {breadcrumbTitle} {breadcrumbItems} />

	<section class="relative py-16 md:py-24">
		<div class="mb-8">
			<form class="relative mx-auto max-w-xl" action="/posts" method="GET">
				<input
					type="text"
					id="search"
					name="search"
					class="h-12 w-full rounded-lg bg-white ps-6 pe-40 pt-4 pb-4 text-black shadow outline-none"
					placeholder="Search"
					value={searchParam}
				/>
				<button
					type="submit"
					class="focus:ring-opacity-25 absolute end-[0] top-[0] inline-block h-12 rounded-e-lg border border-sky-500 bg-sky-500 px-8 py-2.5 align-middle text-[16px] font-medium tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
					><i class="uil uil-search"></i> Search</button
				>
			</form>
		</div>

		<div class="relative container">
			{#if posts.length <= 0}
				<p class="text-center text-gray-500">{message || 'No posts available.'}</p>
			{:else}
				<div class="grid grid-cols-1 gap-[30px] md:grid-cols-2 lg:grid-cols-3">
					{#each posts as post}
						<div
							class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
						>
							<img
								src={post.images
									? apiBaseURL + '/storage/' + post.images
									: '/assets/hoxia-v1/images/blog/1.jpg'}
								alt=""
							/>
							<div class="p-6">
								<span
									class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
									>{post.category_id}</span
								>
								<h5 class="mt-3">
									<a
										href={`/posts/${post.id}`}
										class="title text-lg font-medium duration-500 hover:text-sky-500"
									>
										{@html highlightText(post.judul_berita, searchParam)}
									</a>
								</h5>
								<p class="text-xs text-slate-400">{new Date(post.tanggal).toLocaleDateString()}</p>

								<div class="mt-3 line-clamp-3 text-slate-400">
									{post.content_body}
								</div>

								<div class="mt-4">
									<a
										href={`/posts/${post.id}`}
										class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
										>Read More <i class="uil uil-arrow-right"></i></a
									>
								</div>
							</div>
						</div>
					{/each}
				</div>

				<Pagination {meta_links} {link_first} {link_last} {changePage} />
			{/if}
		</div>
	</section>
</div>
