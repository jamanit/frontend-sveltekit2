<script lang="ts">
	import { onMount } from 'svelte';
	import Breadcrumb from '$lib/components/Breadcrumb.svelte';
	import Button from '$lib/components/Button.svelte';
	import { showToast } from '$lib/utils/toast';

	const baseURL = import.meta.env.VITE_BASE_URL;
</script>

<section>
	<section
		class="relative bg-[url('{baseURL}/assets/hoxia-v1/images/bg/bg1.jpg')] bg-cover bg-center py-36 lg:py-64"
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
				<div class="tiny-six-item">
					<div class="tiny-slide">
						<div
							class="m-2 rounded-md bg-white p-4 text-center shadow dark:bg-slate-900 dark:shadow-gray-800"
						>
							<img
								src="{baseURL}/assets/hoxia-v1/images/shop/biz.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/com.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/me.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/mobi.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/net.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/org.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/tv.jpg"
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
								src="{baseURL}/assets/hoxia-v1/images/shop/us.jpg"
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
					Explore Our Hosting Pricing
				</h3>
				<p class="mx-auto max-w-xl text-slate-400">
					Create, collaborate, and turn your ideas into incredible products with the definitive
					platform for digital design.
				</p>
			</div>

			<div class="mt-8 grid grid-cols-1">
				<ul
					class="mx-auto inline-block w-fit flex-wrap justify-center rounded-full bg-white p-2 text-center shadow dark:bg-slate-900 dark:shadow-gray-800"
					id="myTab"
					data-tabs-toggle="#StarterContent"
					role="tablist"
				>
					<li role="presentation" class="inline-block">
						<button
							class="w-full rounded-full px-4 py-1 text-sm font-semibold transition-all duration-500 ease-in-out hover:text-sky-500"
							id="start-month-tab"
							data-tabs-target="#start-month"
							type="button"
							role="tab"
							aria-controls="start-month"
							aria-selected="true">Monthly</button
						>
					</li>
					<li role="presentation" class="inline-block">
						<button
							class="w-full rounded-full px-4 py-1 text-sm font-semibold transition-all duration-500 ease-in-out"
							id="start-year-tab"
							data-tabs-target="#start-year"
							type="button"
							role="tab"
							aria-controls="start-year"
							aria-selected="false"
							>Yearly <span
								class="ms-1 h-5 rounded-full bg-amber-500 px-2.5 py-0.5 text-xs font-bold text-white"
								>Save 25%</span
							></button
						>
					</li>
				</ul>

				<div id="StarterContent" class="mt-6">
					<div class="" id="start-month" role="tabpanel" aria-labelledby="start-month-tab">
						<div class="grid grid-cols-1 gap-[30px] md:grid-cols-2 lg:grid-cols-4">
							<div
								class="group relative h-fit overflow-hidden rounded-md bg-white p-6 shadow-lg dark:bg-slate-900 dark:shadow-gray-800"
							>
								<h6 class="mb-5 text-xl font-medium">Free</h6>

								<div class="mb-5 flex">
									<span class="text-lg font-medium">$</span>
									<span class="price h6 mb-0 text-5xl font-semibold">0</span>
									<span class="mb-1 self-end text-lg font-medium">/mo</span>
								</div>

								<ul class="list-none text-slate-400">
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">We offers a free month of service for new customers.</span>
									</li>
								</ul>
								<a
									href="/"
									class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-gray-100 bg-transparent px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-slate-900 transition-all duration-500 hover:border-sky-500 hover:bg-sky-500 hover:text-white focus:ring-[3px] focus:ring-sky-500 focus:outline-none dark:border-gray-800 dark:text-white dark:hover:border-sky-500"
									>Free Demo</a
								>
							</div>

							<div
								class="group relative h-fit overflow-hidden rounded-md bg-white p-6 shadow-lg dark:bg-slate-900 dark:shadow-gray-800"
							>
								<h6 class="mb-5 text-xl font-medium">Single</h6>

								<div class="mb-5 flex">
									<span class="text-lg font-medium">$</span>
									<span class="price h6 mb-0 text-5xl font-semibold">9</span>
									<span class="mb-1 self-end text-lg font-medium">/mo</span>
								</div>

								<ul class="list-none text-slate-400">
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">10GB Ram</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">100GB Bandwith</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">100GB SSD Storage</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">3 Domain Hosted Support</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">50 Email Account</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">5 Database</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">Unlimited Traffic</span>
									</li>
								</ul>
								<a
									href="/"
									class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-gray-100 bg-transparent px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-slate-900 transition-all duration-500 hover:border-sky-500 hover:bg-sky-500 hover:text-white focus:ring-[3px] focus:ring-sky-500 focus:outline-none dark:border-gray-800 dark:text-white dark:hover:border-sky-500"
									>Subscribe Now</a
								>
							</div>

							<div
								class="group relative h-fit overflow-hidden rounded-md bg-white shadow-lg dark:bg-slate-900 dark:shadow-gray-800"
							>
								<div
									class="h6 bg-gradient-to-tr from-sky-500 to-blue-700 px-6 py-2 text-lg font-medium text-white"
								>
									Popular
								</div>
								<div class="p-6">
									<h6 class="mb-5 text-xl font-medium">Professional</h6>

									<div class="mb-5 flex">
										<span class="text-lg font-medium">$</span>
										<span class="price h6 mb-0 text-5xl font-semibold">49</span>
										<span class="mb-1 self-end text-lg font-medium">/mo</span>
									</div>

									<ul class="list-none text-slate-400">
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i>
											<span class="mt-0.5"
												>We offers a free 14 days of service for new customers.</span
											>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">100GB Ram</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">1000GB Bandwith</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">1000GB SSD Storage</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">15 Domain Hosted Support</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">100 Email Account</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">10 Database</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">Unlimited Traffic</span>
										</li>
									</ul>
									<a
										href="/"
										class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-sky-500 bg-sky-500 px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
										>Buy Now</a
									>

									<p class="mt-1.5 text-sm text-slate-400">
										<span class="text-red-600">*</span>T&C Apply
									</p>
								</div>
							</div>

							<div
								class="group relative h-fit overflow-hidden rounded-md bg-gradient-to-tr from-sky-500 to-blue-700 p-[1px] shadow-lg dark:shadow-gray-800"
							>
								<div class="rounded-md bg-white p-6 dark:bg-slate-900">
									<h6 class="mb-5 text-xl font-medium">Custom</h6>

									<p class="mb-5 text-slate-400">
										Pricing plan will be as per client or company requirements
									</p>

									<ul class="list-none">
										<li class="mb-1 flex font-medium">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-1">Custom Pricing</span>
										</li>
									</ul>
									<a
										href="/"
										class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-gray-100 bg-transparent px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-slate-900 transition-all duration-500 hover:border-sky-500 hover:bg-sky-500 hover:text-white focus:ring-[3px] focus:ring-sky-500 focus:outline-none dark:border-gray-800 dark:text-white dark:hover:border-sky-500"
										>Talk to us</a
									>
								</div>
							</div>
						</div>
					</div>

					<div class="hidden" id="start-year" role="tabpanel" aria-labelledby="start-year-tab">
						<div class="grid grid-cols-1 gap-[30px] md:grid-cols-2 lg:grid-cols-4">
							<div
								class="group relative h-fit overflow-hidden rounded-md bg-white p-6 shadow-lg dark:bg-slate-900 dark:shadow-gray-800"
							>
								<h6 class="mb-5 text-xl font-medium">Free</h6>

								<div class="mb-5 flex">
									<span class="text-lg font-medium">$</span>
									<span class="price h6 mb-0 text-5xl font-semibold">0</span>
									<span class="mb-1 self-end text-lg font-medium">/year</span>
								</div>

								<ul class="list-none text-slate-400">
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">We offers a free month of service for new customers.</span>
									</li>
								</ul>
								<a
									href="/"
									class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-gray-100 bg-transparent px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-slate-900 transition-all duration-500 hover:border-sky-500 hover:bg-sky-500 hover:text-white focus:ring-[3px] focus:ring-sky-500 focus:outline-none dark:border-gray-800 dark:text-white dark:hover:border-sky-500"
									>Free Demo</a
								>
							</div>

							<div
								class="group relative h-fit overflow-hidden rounded-md bg-white p-6 shadow-lg dark:bg-slate-900 dark:shadow-gray-800"
							>
								<h6 class="mb-5 text-xl font-medium">Single</h6>

								<div class="mb-5 flex">
									<span class="text-lg font-medium">$</span>
									<span class="price h6 mb-0 text-5xl font-semibold">81</span>
									<span class="mb-1 self-end text-lg font-medium">/year</span>
								</div>

								<ul class="list-none text-slate-400">
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">10GB Ram</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">100GB Bandwith</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">100GB SSD Storage</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">3 Domain Hosted Support</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">50 Email Account</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"></i>
										<span class="mt-0.5">5 Database</span>
									</li>
									<li class="mb-1 flex">
										<i class="uil uil-times-circle me-2 align-middle text-[20px] text-red-600"></i>
										<span class="mt-0.5">Unlimited Traffic</span>
									</li>
								</ul>
								<a
									href="/"
									class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-gray-100 bg-transparent px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-slate-900 transition-all duration-500 hover:border-sky-500 hover:bg-sky-500 hover:text-white focus:ring-[3px] focus:ring-sky-500 focus:outline-none dark:border-gray-800 dark:text-white dark:hover:border-sky-500"
									>Subscribe Now</a
								>
							</div>

							<div
								class="group relative h-fit overflow-hidden rounded-md bg-white shadow-lg dark:bg-slate-900 dark:shadow-gray-800"
							>
								<div
									class="h6 bg-gradient-to-tr from-sky-500 to-blue-700 px-6 py-2 text-lg font-medium text-white"
								>
									Popular
								</div>
								<div class="p-6">
									<h6 class="mb-5 text-xl font-medium">Professional</h6>

									<div class="mb-5 flex">
										<span class="text-lg font-medium">$</span>
										<span class="price h6 mb-0 text-5xl font-semibold">441</span>
										<span class="mb-1 self-end text-lg font-medium">/year</span>
									</div>

									<ul class="list-none text-slate-400">
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i>
											<span class="mt-0.5"
												>We offers a free 14 days of service for new customers.</span
											>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">100GB Ram</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">1000GB Bandwith</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">1000GB SSD Storage</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">15 Domain Hosted Support</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">100 Email Account</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">10 Database</span>
										</li>
										<li class="mb-1 flex">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-0.5">Unlimited Traffic</span>
										</li>
									</ul>
									<a
										href="/"
										class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-sky-500 bg-sky-500 px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
										>Buy Now</a
									>

									<p class="mt-1.5 text-sm text-slate-400">
										<span class="text-red-600">*</span>T&C Apply
									</p>
								</div>
							</div>

							<div
								class="group relative h-fit overflow-hidden rounded-md bg-gradient-to-tr from-sky-500 to-blue-700 p-[1px] shadow-lg dark:shadow-gray-800"
							>
								<div class="rounded-md bg-white p-6 dark:bg-slate-900">
									<h6 class="mb-5 text-xl font-medium">Custom</h6>

									<p class="mb-5 text-slate-400">
										Pricing plan will be as per client or company requirements
									</p>

									<ul class="list-none">
										<li class="mb-1 flex font-medium">
											<i class="uil uil-check-circle me-2 align-middle text-[20px] text-sky-500"
											></i> <span class="mt-1">Custom Pricing</span>
										</li>
									</ul>
									<a
										href="/"
										class="focus:ring-opacity-25 mt-5 inline-block w-full rounded-md border border-gray-100 bg-transparent px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-slate-900 transition-all duration-500 hover:border-sky-500 hover:bg-sky-500 hover:text-white focus:ring-[3px] focus:ring-sky-500 focus:outline-none dark:border-gray-800 dark:text-white dark:hover:border-sky-500"
										>Talk to us</a
									>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="relative container mt-16 md:mt-24">
			<div class="grid grid-cols-1 pb-8 text-center">
				<h3 class="mb-4 text-2xl leading-normal font-medium md:text-3xl md:leading-normal">
					Hosting Services
				</h3>
				<p class="mx-auto max-w-xl text-slate-400">
					Create, collaborate, and turn your ideas into incredible products with the definitive
					platform for digital design.
				</p>
			</div>

			<div class="mt-8 grid grid-cols-1 gap-[30px] md:grid-cols-2 lg:grid-cols-4">
				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-server"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Web Hosting</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-cloud-heart"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Domains</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-envelope-check"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Emails</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-users-alt"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Supported</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-tachometer-fast-alt"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Speedy</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-compact-disc"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Reliable</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-weight"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Scalable</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>

				<div
					class="group relative overflow-hidden rounded-md bg-white p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 hover:shadow-md dark:bg-slate-900 dark:shadow-gray-800 dark:hover:bg-sky-500 dark:hover:shadow-gray-700"
				>
					<div class="relative -m-3 overflow-hidden text-transparent">
						<i
							data-feather="hexagon"
							class="h-24 w-24 fill-sky-500/[0.07] group-hover:fill-white/20"
						></i>
						<div
							class="absolute start-8 top-2/4 flex -translate-y-2/4 items-center justify-center rounded-md align-middle text-3xl text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
						>
							<i class="uil uil-invoice"></i>
						</div>
					</div>

					<div class="mt-6">
						<h5>
							<a
								href="/"
								class="text-lg font-medium transition-all duration-500 ease-in-out group-hover:text-white"
								>Easy Upgrade</a
							>
						</h5>
						<p
							class="mt-3 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
						>
							The phrasal sequence of the is now so that many campaign and benefit
						</p>
					</div>
				</div>
			</div>
		</div>

		<div class="relative container mt-16 md:mt-24">
			<div class="mt-10 grid grid-cols-1 items-center gap-[30px] md:grid-cols-2 lg:grid-cols-12">
				<div class="order-1 md:order-2 lg:col-span-6">
					<div class="lg:ms-8">
						<img src="{baseURL}/assets/hoxia-v1/images/2.png" alt="" />
					</div>
				</div>
				<div class="order-2 md:order-1 lg:col-span-6">
					<h3 class="mb-6 text-2xl leading-normal font-medium md:text-3xl md:leading-normal">
						Quick Responce <br /> and Secure Server
					</h3>
					<p class="max-w-xl text-slate-400">
						You can combine all the Hoxia templates into a single one, you can take a component from
						the Application theme and use it in the Website.
					</p>

					<ul class="mt-4 list-none text-slate-400">
						<li class="mb-1 flex">
							<i class="uil uil-check-circle me-2 text-xl text-sky-500"></i> Digital Marketing Solutions
							for Tomorrow
						</li>
						<li class="mb-1 flex">
							<i class="uil uil-check-circle me-2 text-xl text-sky-500"></i> Our Talented & Experienced
							Marketing Agency
						</li>
						<li class="mb-1 flex">
							<i class="uil uil-check-circle me-2 text-xl text-sky-500"></i> Create your own skin to
							match your brand
						</li>
					</ul>

					<div class="mt-4">
						<a
							href="page-aboutus.html"
							class="relative inline-block border-none text-center align-middle text-base tracking-wide text-sky-500 duration-500 ease-in-out after:absolute after:start-0 after:end-0 after:bottom-0 after:h-px after:w-0 after:bg-sky-500 after:transition-all after:duration-500 after:content-[''] hover:text-sky-500 hover:after:end-auto hover:after:w-full"
							>Find Out More <i class="uil uil-angle-right-b align-middle"></i></a
						>
					</div>
				</div>
			</div>
		</div>

		<div class="relative container mt-16 md:mt-24">
			<div class="mt-10 grid grid-cols-1 items-center gap-[30px] md:grid-cols-2 lg:grid-cols-12">
				<div class="lg:col-span-6">
					<div class="lg:me-8">
						<img src="{baseURL}/assets/hoxia-v1/images/3.png" alt="" />
					</div>
				</div>
				<div class="lg:col-span-6">
					<div class="grid grid-cols-1 gap-[30px]">
						<div
							class="group relative flex items-center overflow-hidden rounded-md p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 dark:shadow-gray-800 dark:hover:bg-sky-500"
						>
							<span
								class="text-5xl font-semibold text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
							>
								<i class="uil uil-swatchbook"></i>
							</span>
							<div class="ms-3 flex-1">
								<h5
									class="text-xl font-semibold transition-all duration-500 ease-in-out group-hover:text-white"
								>
									Enhance Security
								</h5>
								<p
									class="mt-2 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
								>
									There are many variations of passages of Lorem Ipsum available
								</p>
							</div>
							<div
								class="text-dark/[0.03] absolute start-1 top-5 text-8xl transition-all duration-500 ease-in-out group-hover:text-white/[0.04] dark:text-white/[0.03]"
							>
								<i class="uil uil-swatchbook"></i>
							</div>
						</div>

						<div
							class="group relative flex items-center overflow-hidden rounded-md p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 dark:shadow-gray-800 dark:hover:bg-sky-500"
						>
							<span
								class="text-5xl font-semibold text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
							>
								<i class="uil uil-tachometer-fast-alt"></i>
							</span>
							<div class="ms-3 flex-1">
								<h5
									class="text-xl font-semibold transition-all duration-500 ease-in-out group-hover:text-white"
								>
									High Performance
								</h5>
								<p
									class="mt-2 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
								>
									There are many variations of passages of Lorem Ipsum available
								</p>
							</div>
							<div
								class="text-dark/[0.03] absolute start-1 top-5 text-8xl transition-all duration-500 ease-in-out group-hover:text-white/[0.04] dark:text-white/[0.03]"
							>
								<i class="uil uil-tachometer-fast-alt"></i>
							</div>
						</div>

						<div
							class="group relative flex items-center overflow-hidden rounded-md p-6 shadow transition-all duration-500 ease-in-out hover:bg-sky-500 dark:shadow-gray-800 dark:hover:bg-sky-500"
						>
							<span
								class="text-5xl font-semibold text-sky-500 transition-all duration-500 ease-in-out group-hover:text-white"
							>
								<i class="uil uil-user-check"></i>
							</span>
							<div class="ms-3 flex-1">
								<h5
									class="text-xl font-semibold transition-all duration-500 ease-in-out group-hover:text-white"
								>
									Unbeatable Support
								</h5>
								<p
									class="mt-2 text-slate-400 transition-all duration-500 ease-in-out group-hover:text-white/50"
								>
									There are many variations of passages of Lorem Ipsum available
								</p>
							</div>
							<div
								class="text-dark/[0.03] absolute start-1 top-5 text-8xl transition-all duration-500 ease-in-out group-hover:text-white/[0.04] dark:text-white/[0.03]"
							>
								<i class="uil uil-user-check"></i>
							</div>
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

		<div class="relative container mt-16 md:mt-24">
			<div
				class="relative overflow-hidden rounded-xl bg-white px-6 py-10 shadow lg:px-8 dark:bg-slate-900 dark:shadow-gray-800"
			>
				<div class="grid grid-cols-1 items-center gap-[30px] md:grid-cols-2">
					<div class="z-1 text-center md:text-start">
						<h3 class="text-2xl leading-normal font-medium md:text-3xl md:leading-normal">
							Subscribe to Newsletter!
						</h3>
						<p class="mx-auto mt-2 max-w-xl text-slate-400">
							Subscribe to get latest updates and information.
						</p>
					</div>

					<div class="subcribe-form z-1">
						<form class="relative max-w-xl">
							<input
								type="email"
								id="subcribe"
								name="email"
								class="h-[50px] w-full rounded-md bg-white py-4 ps-6 pe-40 text-black shadow outline-none dark:bg-slate-900 dark:text-white dark:shadow-gray-800"
								placeholder="Your Email Address :"
							/>
							<button
								type="submit"
								class="focus:ring-opacity-25 absolute end-[3px] top-[2px] inline-block h-[46px] rounded-md border border-sky-500 bg-sky-500 px-8 py-2.5 text-center align-middle text-[16px] font-medium tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
								>Subscribe</button
							>
						</form>
					</div>
				</div>

				<div class="absolute -start-5 -top-5">
					<div
						class="uil uil-envelope -rotate-45 text-7xl text-slate-900/5 lg:text-[150px] dark:text-white/5"
					></div>
				</div>

				<div class="absolute -end-5 -bottom-5">
					<div
						class="uil uil-pen text-7xl text-slate-900/5 lg:text-[150px] dark:text-white/5"
					></div>
				</div>
			</div>
		</div>
	</section>
</section>
