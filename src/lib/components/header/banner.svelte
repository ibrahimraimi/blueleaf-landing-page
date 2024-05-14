<script>
	import * as Avatar from "$lib/components/ui/avatar";
	import { BotMessageSquare, MessageCircle, ShoppingCart } from "lucide-svelte";

	const isLoggedIn = true;
</script>

<section class="flex items-center justify-between">
	<div class="flex items-center justify-center">
		<MessageCircle />
		<span class="text-center">+234 7011642322</span>
	</div>

	<div class="flex items-center justify-between">
		<div
			class="mr-5 hidden cursor-pointer items-center justify-center hover:underline hover:underline-offset-4 lg:flex"
		>
			<BotMessageSquare />
			<span class="ml-2">Quick Chat</span>
		</div>

		{#if !isLoggedIn}
			<Avatar.Root>
				<Avatar.Image src="https://github.com/shadcn.png" alt="@shadcn" />
				<Avatar.Fallback>CN</Avatar.Fallback>
			</Avatar.Root>
		{/if}

		{#if isLoggedIn}
			<div class="ml-4">
				<!-- svelte-ignore a11y-invalid-attribute -->
				<a href="#" class="rounded-full border-none bg-red-600 px-3 py-2 text-white"
					>Create Account</a
				>
				<!-- svelte-ignore a11y-invalid-attribute -->
				<a href="#" class="ml-4 rounded-full border border-black px-3 py-2">Signin</a>
			</div>
		{/if}

		<div class="ml-4 rounded-full bg-gray-200 p-2">
			<ShoppingCart class="text-primary" />
		</div>
	</div>
</section>
