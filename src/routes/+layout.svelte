<!-- src/routes/+layouts.svelte -->
<script lang="ts">
	// import '../app.css';
	import { onMount } from 'svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
	const baseURL = import.meta.env.VITE_BASE_URL;
	const appName = import.meta.env.VITE_APP_NAME;

	function loadScript(src: string): Promise<void> {
		return new Promise((resolve, reject) => {
			const script = document.createElement('script');
			script.src = src;
			script.defer = true;
			script.onload = () => resolve();
			script.onerror = () => reject();
			document.body.appendChild(script);
		});
	}

	onMount(async () => {
		if (typeof window !== 'undefined') {
			try {
				await loadScript(`${baseURL}/assets/hoxia-v1/libs/tiny-slider/min/tiny-slider.js`);
				await loadScript(`${baseURL}/assets/hoxia-v1/js/plugins.init.js`);
				await loadScript(`${baseURL}/assets/hoxia-v1/libs/feather-icons/feather.min.js`);
				await loadScript(`${baseURL}/assets/hoxia-v1/js/app.js`);
			} catch (error) {
				console.error('Error loading scripts:', error);
			}
		}
	});

	onMount(() => {
		document.body.classList.add(
			'font-inter',
			'text-base',
			'text-slate-900',
			'dark:bg-slate-900',
			'dark:text-white'
		);
	});
</script>

<svelte:head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<title>{appName}</title>
	<meta name="description" content="Tailwind CSS Web Hosting Template" />
	<meta
		name="keywords"
		content="creative, modern, Tailwind CSS, multipurpose, clean, cloud hosting, creative hosting, dedicated hosting, email hosting, hosting, html5, modern, reseller hosting, sass, server hosting, service, shop, startup hosting, web hosting"
	/>

	<link href={`${baseURL}/assets/hoxia-v1/images/favicon.ico`} rel="shortcut icon" />
	<link href={`${baseURL}/assets/hoxia-v1/libs/tiny-slider/tiny-slider.css`} rel="stylesheet" />
	<link href={`${baseURL}/assets/hoxia-v1/libs/@iconscout/unicons/css/line.css`} rel="stylesheet" />
	<link
		href={`${baseURL}/assets/hoxia-v1/libs/@mdi/font/css/materialdesignicons.min.css`}
		rel="stylesheet"
	/>
	<link rel="stylesheet" href={`${baseURL}/assets/hoxia-v1/css/tailwind.css`} />
	<script src={`${baseURL}/assets/tailwindcss/cdn-tailwindcss-3.3.3.js`}></script>
</svelte:head>

<!-- <div id="preloader">
	<div id="status">
		<div class="logo !mr-1">
			<img
				src={`${baseURL}/assets/hoxia-v1/images/logo-icon-64.png`}
				class="d-block mx-auto animate-[spin_10s_linear_infinite]"
				alt=""
			/>
		</div>
		<div class="justify-content-center">
			<div class="text-center">
				<h4 class="mt-2 mb-0 text-lg font-semibold">Hoxia</h4>
			</div>
		</div>
	</div>
</div> -->

<Navbar />

{@render children()}

<a
	aria-label="Link"
	id="back-to-top"
	class="back-to-top fixed end-5 bottom-5 z-10 hidden h-9 w-9 cursor-pointer justify-center rounded-full bg-sky-500 text-center text-lg leading-9 text-white"
>
	<i class="uil uil-arrow-up"></i>
</a>

<Footer />

<div class="fixed top-1/3 -right-2 z-3">
	<span class="relative inline-block rotate-90">
		<input type="checkbox" class="checkbox absolute opacity-0" id="chk" />
		<label
			class="label flex h-8 w-14 cursor-pointer items-center justify-between rounded-full bg-slate-900 p-1 shadow dark:bg-white dark:shadow-gray-800"
			for="chk"
		>
			<i class="uil uil-moon text-[20px] text-yellow-500"></i>
			<i class="uil uil-sun text-[20px] text-yellow-500"></i>
			<span
				class="ball absolute top-[2px] left-[2px] h-7 w-7 rounded-full bg-white dark:bg-slate-900"
			></span>
		</label>
	</span>
</div>
