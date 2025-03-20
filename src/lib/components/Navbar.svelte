<script lang="ts">
	import { goto } from '$app/navigation';
	import { isLoggedIn, logout } from '$lib/stores/authStore';

	const appName = import.meta.env.VITE_APP_NAME;
	const baseURL = import.meta.env.VITE_BASE_URL;

	const handleLogout = () => {
		logout();
		goto('/login');
	};
</script>

<!-- 
<nav class="flex items-center bg-purple-800 px-4 py-4 text-white md:px-24">
	<h1 class="text-xl font-bold">{appName}</h1>
	<div class="ml-auto">
		<a href="/" class="mr-4">Home</a>
		<a href="/about" class="mr-4" data-sveltekit-prefetch>About</a>

		{#if $isLoggedIn}
			<a href="/admin" class="mr-4" data-sveltekit-prefetch>Dashboard</a>
			<a href="/admin/me" class="mr-4" data-sveltekit-prefetch>Me</a>
			<a href="/admin/users" class="mr-4" data-sveltekit-prefetch>Users</a>
			<button
				class="cursor-pointer rounded-lg bg-red-500 px-4 py-2 text-white hover:bg-red-600 focus:outline-none focus:ring-2 focus:ring-red-500"
				on:click={handleLogout}
			>
				Logout
			</button>
		{:else}
			<a href="/login" class="mr-4" data-sveltekit-prefetch>Login</a>
			<a href="/register" class="mr-4" data-sveltekit-prefetch>Register</a>
		{/if}
	</div>
</nav> -->

<nav id="topnav" class="defaultscroll is-sticky">
	<div class="relative container flex">
		<!-- Logo container-->
		<a class="logo mr-auto" href="index.html">
			<span class="inline-block dark:hidden">
				<img src="{baseURL}/assets/hoxia-v1/images/logo-dark.png" class="l-dark h-7" alt="" />
				<img src="{baseURL}/assets/hoxia-v1/images/logo-light.png" class="l-light h-7" alt="" />
			</span>
			<img
				src="{baseURL}/assets/hoxia-v1/images/logo-white.png"
				class="hidden h-7 dark:inline-block"
				alt=""
			/>
		</a>
		<!-- End Logo container-->

		<div id="navigation">
			<!-- Navigation Menu-->
			<ul class="navigation-menu nav-light justify-end">
				<li><a href="/" data-sveltekit-prefetch class="sub-menu-item">Home</a></li>

				<li class="has-submenu parent-parent-menu-item">
					<a href="javascript:void(0)"> Hosting </a><span class="menu-arrow"></span>
					<ul class="submenu">
						<li><a href="hosting-shared.html" class="sub-menu-item">Shared Hosting</a></li>
						<li><a href="hosting-vps.html" class="sub-menu-item">VPS Hosting</a></li>
						<li>
							<a href="hosting-dedicated.html" class="sub-menu-item">Dedicated Server</a>
						</li>
						<li><a href="hosting-cloud.html" class="sub-menu-item">Cloud Hosting</a></li>
						<li><a href="hosting-domain.html" class="sub-menu-item">Domain Name</a></li>
						<li>
							<a href="hosting-reseller.html" class="sub-menu-item">Reseller Hosting</a>
						</li>
					</ul>
				</li>

				<li class="has-submenu parent-parent-menu-item">
					<a href="javascript:void(0)"> Domain </a><span class="menu-arrow"></span>
					<ul class="submenu">
						<li><a href="domain-detail.html" class="sub-menu-item">Domain Detail</a></li>
						<li><a href="cart.html" class="sub-menu-item">Cart</a></li>
						<li><a href="checkouts.html" class="sub-menu-item">Checkout</a></li>
						<li><a href="my-account.html" class="sub-menu-item">Account</a></li>
					</ul>
				</li>

				<li class="has-submenu parent-parent-menu-item">
					<a href="javascript:void(0)">Pages</a><span class="menu-arrow"></span>
					<ul class="submenu">
						<li class="has-submenu parent-menu-item">
							<a href="javascript:void(0)"> Helpcenter </a><span class="submenu-arrow"></span>
							<ul class="submenu">
								<li><a href="helpcenter-overview.html" class="sub-menu-item">Overview</a></li>
								<li><a href="helpcenter-faqs.html" class="sub-menu-item">FAQs</a></li>
								<li><a href="helpcenter-guides.html" class="sub-menu-item">Guides</a></li>
								<li><a href="helpcenter-support.html" class="sub-menu-item">Support</a></li>
							</ul>
						</li>

						<li class="has-submenu parent-menu-item">
							<a href="javascript:void(0)"> Blog </a><span class="submenu-arrow"></span>
							<ul class="submenu">
								<li><a href="blogs.html" class="sub-menu-item"> Blogs</a></li>
								<li><a href="blog-detail.html" class="sub-menu-item"> Blog Detail</a></li>
							</ul>
						</li>

						<li class="has-submenu parent-menu-item">
							<a href="javascript:void(0)"> Auth Pages </a><span class="submenu-arrow"></span>
							<ul class="submenu">
								<li><a href="login.html" class="sub-menu-item"> Login</a></li>
								<li><a href="signup.html" class="sub-menu-item"> Signup</a></li>
								<li>
									<a href="reset-password.html" class="sub-menu-item"> Forgot Password</a>
								</li>
								<li><a href="lock-screen.html" class="sub-menu-item"> Lock Screen</a></li>
							</ul>
						</li>

						<li class="has-submenu parent-menu-item">
							<a href="javascript:void(0)"> Utility </a><span class="submenu-arrow"></span>
							<ul class="submenu">
								<li><a href="terms.html" class="sub-menu-item">Terms of Services</a></li>
								<li><a href="privacy.html" class="sub-menu-item">Privacy Policy</a></li>
							</ul>
						</li>

						<li class="has-submenu parent-menu-item">
							<a href="javascript:void(0)"> Special </a><span class="submenu-arrow"></span>
							<ul class="submenu">
								<li><a href="comingsoon.html" class="sub-menu-item"> Coming Soon</a></li>
								<li><a href="maintenance.html" class="sub-menu-item"> Maintenance</a></li>
								<li><a href="error.html" class="sub-menu-item"> 404!</a></li>
								<li><a href="thankyou.html" class="sub-menu-item"> Thank you</a></li>
							</ul>
						</li>
					</ul>
				</li>

				<li><a href="contact.html" class="sub-menu-item">Contact</a></li>
			</ul>
			<!--end navigation menu-->
		</div>
		<!--end navigation-->

		<!--Login button Start-->
		<ul class="buy-button mb-0 list-none">
			<li class="dropdown relative inline-block">
				<button
					data-dropdown-toggle="dropdown"
					class="dropdown-toggle focus:ring-opacity-25 inline-flex h-8 w-8 items-center justify-center rounded-full border border-sky-500 bg-sky-500 text-center align-middle text-base text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
					type="button"
				>
					<i class="uil uil-search"></i>
				</button>
				<!-- Dropdown menu -->
				<div
					class="dropdown-menu absolute end-0 z-10 m-0 mt-4 hidden w-48 overflow-hidden rounded-md bg-white shadow dark:bg-slate-900 dark:shadow-gray-800"
					on:click={(event) => event.stopPropagation()}
				>
					<div class="relative">
						<i class="uil uil-search absolute end-3 top-[3px] text-lg"></i>
						<input
							type="text"
							class="form-input h-9 w-36 border-none bg-white pe-10 focus:ring-0 sm:w-44 dark:bg-slate-900"
							name="s"
							id="navSearch"
							placeholder="Search..."
						/>
					</div>
				</div>
			</li>

			<li class="dropdown relative inline-block ps-1">
				<button
					data-dropdown-toggle="dropdown"
					class="dropdown-toggle focus:ring-opacity-25 inline-flex h-8 w-8 items-center justify-center rounded-full border border-sky-500 bg-sky-500 text-center align-middle text-base text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
					type="button"
				>
					<img src="{baseURL}/assets/hoxia-v1/images/flags/usa.png" alt="" />
				</button>
				<!-- Dropdown menu -->
				<div
					class="dropdown-menu absolute end-0 z-10 m-0 mt-4 hidden w-36 overflow-hidden rounded-md bg-white shadow dark:bg-slate-900 dark:shadow-gray-800"
					on:click={(event) => event.stopPropagation()}
				>
					<ul class="py-2 text-start">
						<li class="my-1">
							<a
								href=""
								class="flex items-center px-4 py-1.5 text-[14px] font-medium hover:text-sky-500"
								><img
									src="{baseURL}/assets/hoxia-v1/images/flags/germany.png"
									class="me-2 h-6 w-6 rounded-full shadow dark:shadow-gray-800"
									alt=""
								/> German</a
							>
						</li>
						<li class="my-1">
							<a
								href=""
								class="flex items-center px-4 py-1.5 text-[14px] font-medium hover:text-sky-500"
								><img
									src="{baseURL}/assets/hoxia-v1/images/flags/italy.png"
									class="me-2 h-6 w-6 rounded-full shadow dark:shadow-gray-800"
									alt=""
								/> Italian</a
							>
						</li>
						<li class="my-1">
							<a
								href=""
								class="flex items-center px-4 py-1.5 text-[14px] font-medium hover:text-sky-500"
								><img
									src="{baseURL}/assets/hoxia-v1/images/flags/russia.png"
									class="me-2 h-6 w-6 rounded-full shadow dark:shadow-gray-800"
									alt=""
								/> Russian</a
							>
						</li>
						<li class="my-1">
							<a
								href=""
								class="flex items-center px-4 py-1.5 text-[14px] font-medium hover:text-sky-500"
								><img
									src="{baseURL}/assets/hoxia-v1/images/flags/spain.png"
									class="me-2 h-6 w-6 rounded-full shadow dark:shadow-gray-800"
									alt=""
								/> Spanish</a
							>
						</li>
					</ul>
				</div>
			</li>

			<li class="dropdown relative inline-block ps-1">
				<button
					data-dropdown-toggle="dropdown"
					class="dropdown-toggle focus:ring-opacity-25 inline-flex h-8 w-8 items-center justify-center rounded-full border border-sky-500 bg-sky-500 text-center align-middle text-base text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
					type="button"
				>
					<i class="uil uil-shopping-bag"></i>
				</button>
				<!-- Dropdown menu -->
				<div
					class="dropdown-menu absolute end-0 z-10 m-0 mt-4 hidden w-60 overflow-hidden rounded-md bg-white shadow dark:bg-slate-900 dark:shadow-gray-800"
					on:click={(event) => event.stopPropagation()}
				>
					<ul class="py-3 text-start">
						<li>
							<a href="#" class="flex items-center justify-between px-4 py-1.5">
								<span class="flex items-center">
									<img
										src="{baseURL}/assets/hoxia-v1/images/shop/com.jpg"
										class="w-9 rounded shadow dark:shadow-gray-800"
										alt=""
									/>
									<span class="ms-3">
										<span class="h6 block text-[16px] font-medium hover:text-sky-500"
											>hoxia.com</span
										>
										<span class="block text-sm text-slate-400">$12</span>
									</span>
								</span>

								<span class="text-sm font-semibold">$12</span>
							</a>
						</li>

						<li class="my-2 border-t border-gray-100 dark:border-gray-800"></li>

						<li class="flex items-center justify-between px-4 py-1.5">
							<h6 class="mb-0 font-medium">Total($):</h6>
							<h6 class="mb-0 font-medium">$12</h6>
						</li>

						<li class="px-4 py-1.5">
							<a
								href="javascript:void(0)"
								class="focus:ring-opacity-25 inline-block rounded-lg border border-sky-500 bg-sky-500 px-4 py-[6px] align-middle text-sm tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
								>View Cart</a
							>
							<a
								href="javascript:void(0)"
								class="focus:ring-opacity-25 inline-block rounded-lg border border-sky-500 bg-sky-500 px-4 py-[6px] align-middle text-sm tracking-wide text-white transition-all duration-500 hover:border-sky-600 hover:bg-sky-600 focus:ring-[3px] focus:ring-sky-500 focus:outline-none"
								>Checkout</a
							>
							<p class="mt-1 text-sm text-slate-400">*T&C Apply</p>
						</li>
					</ul>
				</div>
			</li>
		</ul>
		<!--Login button End-->

		<!-- Start Mobile Toggle -->
		<div class="menu-extras">
			<div class="menu-item">
				<a aria-label="Link" class="navbar-toggle" id="isToggle">
					<div class="lines">
						<span></span>
						<span></span>
						<span></span>
					</div>
				</a>
			</div>
		</div>
		<!-- End Mobile Toggle -->
	</div>
	<!--end container-->
</nav>
