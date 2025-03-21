<script lang="ts">
	import { onMount } from 'svelte';
	import Breadcrumb from '$lib/components/Breadcrumb.svelte';
	import Button from '$lib/components/Button.svelte';
	import { showToast } from '$lib/utils/toast';

	const baseURL = import.meta.env.VITE_BASE_URL;
</script>

<section>
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
					<form class="relative mx-auto max-w-xl">
						<input
							type="text"
							id="searchDomain"
							name="text"
							class="h-12 w-full rounded-lg bg-white ps-6 pe-40 pt-4 pb-4 text-black shadow outline-none"
							placeholder="Search Your Domain"
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
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-900 dark:shadow-gray-800"
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
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-900 dark:shadow-gray-800"
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
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-900 dark:shadow-gray-800"
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
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-900 dark:shadow-gray-800"
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

		<div class="relative container mt-16 md:mt-24">
			<div class="grid grid-cols-1 pb-8 text-center">
				<h3 class="mb-4 text-2xl leading-normal font-medium md:text-3xl md:leading-normal">
					Latest Post
				</h3>
				<p class="mx-auto max-w-xl text-slate-400">
					Create, collaborate, and turn your ideas into incredible products with the definitive
					platform for digital design.
				</p>
			</div>

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
			</div>
		</div>

		<div class="relative container mt-16 md:mt-24">
			<div class="grid grid-cols-1 pb-8 text-center">
				<h3 class="mb-4 text-2xl leading-normal font-medium md:text-3xl md:leading-normal">
					Frequently Asked Questions
				</h3>

				<p class="mx-auto max-w-xl text-slate-400">
					Create, collaborate, and turn your ideas into incredible products with the definitive
					platform for digital design.
				</p>
			</div>

			<div
				id="accordion-collapse"
				data-accordion="collapse"
				class="mt-8 grid grid-cols-1 md:grid-cols-2 md:gap-[30px]"
			>
				<div>
					<div class="relative overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-1">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-1"
								aria-expanded="true"
								aria-controls="accordion-collapse-body-1"
							>
								<span class="text-[17px]">How does it work ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0 rotate-180"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-1"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-1"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>

					<div class="relative mt-4 overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-2">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-2"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-2"
							>
								<span class="text-[17px]">Do I need a designer to use Hoxia ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-2"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-2"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>

					<div class="relative mt-4 overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-3">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-3"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-3"
							>
								<span class="text-[17px]">What do I need to do to start selling ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-3"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-3"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>

					<div class="relative mt-4 overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-4">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-4"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-4"
							>
								<span class="text-[17px]">What happens when I receive an order ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-4"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-4"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>
				</div>

				<div>
					<div class="relative mt-4 overflow-hidden rounded-md shadow md:mt-0 dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-5">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-5"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-5"
							>
								<span class="text-[17px]">How does it work ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0 rotate-180"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-5"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-5"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>

					<div class="relative mt-4 overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-6">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-6"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-6"
							>
								<span class="text-[17px]">Do I need a designer to use Hoxia ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-6"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-6"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>

					<div class="relative mt-4 overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-7">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-7"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-7"
							>
								<span class="text-[17px]">What do I need to do to start selling ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-7"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-7"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>

					<div class="relative mt-4 overflow-hidden rounded-md shadow dark:shadow-gray-800">
						<h2 class="text-base font-semibold" id="accordion-collapse-heading-8">
							<button
								type="button"
								class="flex w-full items-center justify-between p-5 text-start font-medium"
								data-accordion-target="#accordion-collapse-body-8"
								aria-expanded="false"
								aria-controls="accordion-collapse-body-8"
							>
								<span class="text-[17px]">What happens when I receive an order ?</span>
								<svg
									data-accordion-icon
									class="h-4 w-4 shrink-0"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									></path>
								</svg>
							</button>
						</h2>
						<div
							id="accordion-collapse-body-8"
							class="hidden"
							aria-labelledby="accordion-collapse-heading-8"
						>
							<div class="p-5">
								<p class="text-slate-400 dark:text-gray-400">
									There are many variations of passages of Lorem Ipsum available, but the majority
									have suffered alteration in some form.
								</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</section>
