<script lang="ts">
	import { Menu } from "lucide-svelte";
	import Separator from "../ui/separator/separator.svelte";
	import * as Sheet from "$lib/components/ui/sheet/index.js";
	import { Button } from "$lib/components/ui/button/index.js";

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

<Sheet.Root>
	<Sheet.Trigger asChild let:builder>
		<Button builders={[builder]} variant="link" size="icon">
			<Menu />
		</Button>
	</Sheet.Trigger>
	<Sheet.Content side="right">
		<Sheet.Header>
			<Sheet.Title>
				<div>
					<span><img src="./logo.svg" width="100" alt="logo" /></span>
				</div>
			</Sheet.Title>

			<Separator />
		</Sheet.Header>
		<div class="mt-5">
			<ul class="flex flex-col items-start">
				{#each navLinks as link}
					<li class="ml-4">
						<a href={link.path} class="hover:underline hover:underline-offset-4">{link.label}</a>
					</li>
				{/each}
			</ul>
		</div>
	</Sheet.Content>
</Sheet.Root>
