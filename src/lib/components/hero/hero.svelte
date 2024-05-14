<script>
	import Input from "../ui/input/input.svelte";
</script>

<section class="body-font">
	<div class="flex flex-col items-center px-5 py-20 md:flex-row">
		<div
			class="mb-16 flex flex-col items-center text-center md:mb-0 md:w-1/2 md:items-start md:pr-16 md:text-left lg:flex-grow lg:pr-24"
		>
			<h1 class="title-font mb-4 text-4xl font-extrabold leading-none text-blue-700 lg:text-[5rem]">
				We brand and deliver quality prints...
			</h1>

			<div class="mt-5">
				<Input placeholder="Search All Products..." class="rounded-full" />
			</div>
		</div>
		<div class="w-5/6 md:w-1/2 lg:w-full lg:max-w-lg">
			<img
				class="rounded object-cover object-center"
				alt="hero"
				src="https://dummyimage.com/720x600"
			/>
		</div>
	</div>
</section>
