<script lang="ts">
	import { onMount } from 'svelte';
	import Breadcrumb from '$lib/components/Breadcrumb.svelte';
	import Button from '$lib/components/Button.svelte';
	import { showToast } from '$lib/utils/toast';
	import Pagination from '$lib/components/Pagination.svelte';

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
	let posts: Post[] = [];
	let meta_links: MetaLink[] = [];
	// let meta_total: number | null = null;
	// let meta_current_page: number | null = null;
	// let meta_per_page: number | null = null;
	// let meta_last_page: number | null = null;
	// let meta_from: number | null = null;
	let link_first: string | null = '';
	let link_last: string | null = '';
	let message = '';

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
			// meta_total = result.meta.total;
			// meta_current_page = result.meta.current_page;
			// meta_per_page = result.meta.per_page;
			// meta_last_page = result.meta.last_page;
			// meta_from = result.meta.from;
			link_first = result.links.first;
			link_last = result.links.last;
		} catch (err) {
			message = 'Error fetching posts.';
			console.error(err);
		}
	}

	onMount(() => {
		getPosts(postUrl);
	});

	function changePage(postUrl: String) {
		if (postUrl) {
			getPosts(postUrl);
		}
	}
</script>

<section>
	<nav class="bg-gray-500 py-[37px]"></nav>
	<section
		class="relative table w-full bg-[url({`${baseURL}/assets/hoxia-v1/images/bg/bg5.png`})] bg-cover bg-center py-36 md:py-40"
	>
		<div class="absolute inset-0 bg-sky-500/5"></div>
		<div class="relative container">
			<div class="mt-12 grid grid-cols-1 text-center">
				<h3 class="text-3xl leading-snug font-medium md:text-4xl md:leading-snug">Latest Post</h3>
			</div>
		</div>

		<div class="absolute start-0 end-0 bottom-5 z-10 mx-3 text-center">
			<ul class="mb-0 inline-block tracking-[0.5px]">
				<li
					class="inline-block text-[15px] font-medium duration-500 ease-in-out hover:text-sky-500"
				>
					<a href="/" data-sveltekit-prefetch>Home</a>
				</li>
				<li class="inline-block text-[15px] ltr:rotate-0 rtl:rotate-180">
					<i class="mdi mdi-chevron-right"></i>
				</li>
				<li class="inline-block text-[15px] font-medium text-sky-500 duration-500 ease-in-out">
					Posts
				</li>
			</ul>
		</div>
	</section>

	<div class="relative">
		<div
			class="shape absolute start-0 end-0 -bottom-[2px] z-1 overflow-hidden text-white sm:-bottom-px dark:text-slate-900"
		>
			<svg
				class="h-auto w-full"
				viewBox="0 0 2880 48"
				fill="none"
				xmlns="http://www.w3.org/2000/svg"
			>
				<path d="M0 48H1437.5H2880V0H2160C1442.5 52 720 0 720 0H0V48Z" fill="currentColor"></path>
			</svg>
		</div>
	</div>

	<section class="relative py-16 md:py-24">
		<div class="relative container">
			{#if posts.length < 0}
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
										>{post.judul_berita}</a
									>
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
</section>
