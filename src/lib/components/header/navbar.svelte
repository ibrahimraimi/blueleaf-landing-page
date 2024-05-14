<script>
	import { Menu } from "lucide-svelte";
	import Separator from "../ui/separator/separator.svelte";
	import Banner from "./banner.svelte";
	import Sidebar from "./sidebar.svelte";
	import Input from "../ui/input/input.svelte";

	const navLinks = [
		{
			label: "Home",
			path: "/"
		},
		{
			label: "About Us",
			path: "/about"
		},
		{
			label: "All Products",
			path: "/products"
		},
		{
			label: "Become A Reseller",
			path: "/re-seller"
		}
	];
</script>

<section>
	<Banner />
	<Separator class="my-4 hidden" />

	<nav class="flex items-center justify-between">
		<div>
			<span><img src="./logo.svg" width="100" alt="logo" /></span>
		</div>

		<div class="hidden items-center justify-center lg:flex">
			<ul class="flex items-center">
				{#each navLinks as link}
					<li class="ml-4">
						<a href={link.path} class="hover:underline hover:underline-offset-4">{link.label}</a>
					</li>
				{/each}
			</ul>
		</div>

		<div class="rounded-full bg-gray-200 p-1 lg:hidden">
			<Sidebar />
		</div>
	</nav>
</section>
