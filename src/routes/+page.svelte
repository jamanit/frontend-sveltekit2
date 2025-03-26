<script lang="ts">
	import { onMount } from 'svelte';
	import Breadcrumb from '$lib/components/Breadcrumb.svelte';
	import Button from '$lib/components/Button.svelte';
	import { showToast } from '$lib/utils/toast';

	const baseURL = import.meta.env.VITE_BASE_URL;
	const apiBaseURL = import.meta.env.VITE_API_BASE_URL;

	// type Category = {
	// 	name: string;
	// };

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
		// category: Category;
	};

	let posts: Post[] = [];
	let message = '';

	async function getPosts() {
		try {
			const response = await fetch(apiBaseURL + `/api/posts`, {
				method: 'GET'
			});
			if (!response.ok) {
				throw new Error(`Failed to fetch: ${response.status}`);
			}
			const result = await response.json();
			posts = result.data;
			console.log(posts);
		} catch (err) {
			message = 'Error fetching posts.';
			console.error(err);
		}
	}

	onMount(() => {
		getPosts();
	});
</script>

<div>
	<section
		class="relative bg-[url({`${baseURL}/assets/hoxia-v1/images/bg/bg1.jpg`})] bg-cover bg-center py-36 lg:py-64"
	>
		<div class="absolute inset-0 bg-gradient-to-b from-slate-950 to-transparent"></div>
		<div class="relative container">
			<div class="mt-10 grid grid-cols-1 items-center text-center">
				<h4
					class="mb-5 text-4xl leading-normal font-semibold text-white lg:text-5xl lg:leading-normal"
				>
					Choose your web hosting <br /> plan for
					<span class="typewrite text-yellow-500">
						<span class="wrap"></span>
					</span>
				</h4>
				<p class="mx-auto max-w-xl text-lg text-white/70">
					Create, collaborate, and turn your ideas into incredible products with the definitive
					platform for digital design.
				</p>

				<div class="mt-6">
					<form class="relative mx-auto max-w-xl" action="/posts" method="GET">
						<input
							type="text"
							id="search"
							name="search"
							class="h-12 w-full rounded-lg bg-white ps-6 pe-40 pt-4 pb-4 text-black shadow outline-none"
							placeholder="Search"
						/>
						<button
							type="submit"
							class="focus:ring-opacity-25 absolute end-[0] top-[0] inline-block h-12 rounded-e-lg border border-sky-500 bg-sky-500 px-8 py-2.5 align-middle text-[16px] font-medium tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
							><i class="uil uil-search"></i> Search</button
						>
					</form>
				</div>
			</div>
		</div>
	</section>

	<section class="relative -mt-[74px] pb-16 md:pb-24">
		<div class="relative container">
			<div class="relative grid grid-cols-1">
				<div class="tiny-four-item">
					<div class="tiny-slide">
						<div
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-800 dark:shadow-gray-800"
						>
							<img
								src={`${baseURL}/assets/hoxia-v1/images/shop/biz.jpg`}
								class="mx-auto mb-3 h-16 w-16 rounded-md shadow dark:shadow-gray-800"
								alt=""
							/>
							<span class="mt-2 flex justify-center">
								<span class="text-base text-slate-400">$</span>
								<span class="h6 mx-1 text-lg font-semibold">3.99</span>
								<span class="self-end text-base text-slate-400">/year</span>
							</span>
						</div>
					</div>

					<div class="tiny-slide">
						<div
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-800 dark:shadow-gray-800"
						>
							<img
								src={`${baseURL}/assets/hoxia-v1/images/shop/com.jpg`}
								class="mx-auto mb-3 h-16 w-16 rounded-md shadow dark:shadow-gray-800"
								alt=""
							/>
							<span class="mt-2 flex justify-center">
								<span class="text-base text-slate-400">$</span>
								<span class="h6 mx-1 text-lg font-semibold">3.99</span>
								<span class="self-end text-base text-slate-400">/year</span>
							</span>
						</div>
					</div>

					<div class="tiny-slide">
						<div
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-800 dark:shadow-gray-800"
						>
							<img
								src={`${baseURL}/assets/hoxia-v1/images/shop/me.jpg`}
								class="mx-auto mb-3 h-16 w-16 rounded-md shadow dark:shadow-gray-800"
								alt=""
							/>
							<span class="mt-2 flex justify-center">
								<span class="text-base text-slate-400">$</span>
								<span class="h6 mx-1 text-lg font-semibold">3.99</span>
								<span class="self-end text-base text-slate-400">/year</span>
							</span>
						</div>
					</div>

					<div class="tiny-slide">
						<div
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-800 dark:shadow-gray-800"
						>
							<img
								src={`${baseURL}/assets/hoxia-v1/images/shop/mobi.jpg`}
								class="mx-auto mb-3 h-16 w-16 rounded-md shadow dark:shadow-gray-800"
								alt=""
							/>
							<span class="mt-2 flex justify-center">
								<span class="text-base text-slate-400">$</span>
								<span class="h6 mx-1 text-lg font-semibold">3.99</span>
								<span class="self-end text-base text-slate-400">/year</span>
							</span>
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="relative container pt-16 pb-8 md:pt-24 md:pb-12">
			<div class="grid grid-cols-1 pb-8 text-center">
				<h3 class="mb-4 text-2xl leading-normal font-medium md:text-3xl md:leading-normal">
					Latest Post
				</h3>
				<p class="mx-auto max-w-xl text-slate-400">
					Create, collaborate, and turn your ideas into incredible products with the definitive
					platform for digital design.
				</p>
			</div>

			{#if posts.length === 0}
				<p class="text-center text-gray-500">Loading...</p>
			{:else}
				<div class="grid grid-cols-1 gap-[30px] md:grid-cols-2 lg:grid-cols-3">
					{#each posts as post}
						<div
							class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:bg-slate-800 dark:shadow-gray-800"
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

				<div class="mt-6 flex items-center justify-center">
					<a
						href="/posts"
						class="rounded-lg bg-sky-600 px-4 py-2 text-base text-white hover:bg-sky-700"
						>View all posts</a
					>
				</div>
			{/if}
		</div>
	</section>
</div>
