<script lang="ts">
	import { onMount } from 'svelte';
	import Breadcrumb from '$lib/components/Breadcrumb.svelte';
	import Button from '$lib/components/Button.svelte';
	import { showToast } from '$lib/utils/toast';

	const baseURL = import.meta.env.VITE_BASE_URL;
</script>

<section>
	<!-- Start -->
	<nav class="bg-gray-500 py-[37px]"></nav>
	<section
		class="relative table w-full bg-[url({`${baseURL}/assets/hoxia-v1/images/bg/bg5.jpg`})] bg-cover bg-center py-36 md:py-40"
	>
		<div class="absolute inset-0 bg-sky-500/5"></div>
		<div class="relative container">
			<div class="mt-12 grid grid-cols-1 text-center">
				<h3 class="text-3xl leading-snug font-medium md:text-4xl md:leading-snug">Latest Post</h3>
			</div>
			<!--end grid-->
		</div>
		<!--end container-->

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
	<!--end section-->
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
	<!-- End Hero -->

	<!-- Start -->
	<section class="relative py-16 md:py-24">
		<div class="relative container">
			<div class="grid grid-cols-1 gap-[30px] md:grid-cols-2 lg:grid-cols-3">
				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/1.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Quickly formulate backend</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/2.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Progressively visualize enabled</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/3.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Credibly implement maximizing</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/4.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Quickly formulate backend</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/5.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Progressively visualize enabled</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/6.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Credibly implement maximizing</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/7.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Quickly formulate backend</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/8.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Progressively visualize enabled</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->

				<div
					class="group relative overflow-hidden rounded-md shadow transition duration-500 hover:shadow-md dark:shadow-gray-800"
				>
					<img src={`${baseURL}/assets/hoxia-v1/images/blog/9.jpg`} alt="" />

					<div class="p-6">
						<span
							class="ms-1 h-5 rounded-full bg-sky-500/5 px-2.5 py-0.5 text-xs font-semibold text-sky-500"
							>VPS Hosting</span
						>

						<h5 class="mt-3">
							<a
								href="blog-detail.html"
								class="title text-lg font-medium duration-500 hover:text-sky-500"
								>Credibly implement maximizing</a
							>
						</h5>

						<p class="mt-3 text-slate-400">
							The phrasal sequence of the is now so that many campaign and benefit
						</p>

						<div class="mt-4">
							<a
								href="blog-detail.html"
								class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
								>Read More <i class="uil uil-arrow-right"></i></a
							>
						</div>
					</div>
				</div>
				<!--end content-->
			</div>
			<!--end grid-->

			<div class="mt-8 grid grid-cols-1 md:grid-cols-12">
				<div class="text-center md:col-span-12">
					<nav aria-label="Page navigation example">
						<ul class="inline-flex items-center -space-x-px">
							<li>
								<a
									href="#"
									class="inline-flex h-[40px] w-[40px] items-center justify-center rounded-s-3xl border border-gray-100 bg-white text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
								>
									<i class="uil uil-angle-left text-[20px] rtl:-mt-1 rtl:rotate-180"></i>
								</a>
							</li>
							<li>
								<a
									href="#"
									class="inline-flex h-[40px] w-[40px] items-center justify-center border border-gray-100 bg-white text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
									>1</a
								>
							</li>
							<li>
								<a
									href="#"
									class="inline-flex h-[40px] w-[40px] items-center justify-center border border-gray-100 bg-white text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
									>2</a
								>
							</li>
							<li>
								<a
									href="#"
									aria-current="page"
									class="z-10 inline-flex h-[40px] w-[40px] items-center justify-center border border-sky-500 bg-sky-500 text-white"
									>3</a
								>
							</li>
							<li>
								<a
									href="#"
									class="inline-flex h-[40px] w-[40px] items-center justify-center border border-gray-100 bg-white text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
									>4</a
								>
							</li>
							<li>
								<a
									href="#"
									class="inline-flex h-[40px] w-[40px] items-center justify-center border border-gray-100 bg-white text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
									>5</a
								>
							</li>
							<li>
								<a
									href="#"
									class="inline-flex h-[40px] w-[40px] items-center justify-center rounded-e-3xl border border-gray-100 bg-white text-slate-400 hover:border-sky-500 hover:bg-sky-500 hover:text-white dark:border-gray-800 dark:bg-slate-900 dark:hover:border-sky-500 dark:hover:bg-sky-500"
								>
									<i class="uil uil-angle-right text-[20px] rtl:-mt-1 rtl:rotate-180"></i>
								</a>
							</li>
						</ul>
					</nav>
				</div>
				<!--end col-->
			</div>
			<!--end grid-->
		</div>
		<!--end container-->
	</section>
	<!--end section-->
	<!-- End -->
</section>
