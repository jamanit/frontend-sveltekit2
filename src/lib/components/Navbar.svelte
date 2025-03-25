<script lang="ts">
	const appName = import.meta.env.VITE_APP_NAME;
	const baseURL = import.meta.env.VITE_BASE_URL;
</script>

<nav id="topnav" class="defaultscroll is-sticky">
	<div class="relative container flex">
		<!-- Logo container-->
		<a class="logo mr-auto" href="/">
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

				<li><a href="/posts" data-sveltekit-prefetch class="sub-menu-item">Posts</a></li>

				<li class="has-submenu parent-parent-menu-item">
					<a href="javascript:void(0)"> Domain </a><span class="menu-arrow"></span>
					<ul class="submenu">
						<li><a href="domain-detail.html" class="sub-menu-item">Domain Detail</a></li>
						<li><a href="cart.html" data-sveltekit-prefetch class="sub-menu-item">Cart</a></li>
						<li>
							<a href="checkouts.html" data-sveltekit-prefetch class="sub-menu-item">Checkout</a>
						</li>
						<li>
							<a href="my-account.html" data-sveltekit-prefetch class="sub-menu-item">Account</a>
						</li>
					</ul>
				</li>
			</ul>
			<!--end navigation menu-->
		</div>
		<!--end navigation-->

		<!--Login button Start-->
		<ul class="buy-button mb-0 list-none">
			<li class="dropdown relative inline-block">
				<button
					aria-label="Button"
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
