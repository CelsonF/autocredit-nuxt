<template>
	<div>
		<NuxtLayout>
			<NuxtPage />
		</NuxtLayout>
	</div>
</template>

<script setup lang="ts">
useHead({
	title: 'Autocredit',
	meta: [
		{ name: 'description', content: 'Seu site de consulta veicular e análise de crédito.' }
	],
	bodyAttrs: {
		class: 'test'
	},
	link: [
		{
			rel: "stylesheet",
			href: "https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;500;700;800&display=swap"
		},
		{
			rel: "preconnect",
			href: "https://fonts.googleapis.com"
		},
		{
			rel: "preconnect",
			href: "https://fonts.gstatic.com",
			crossorigin: 'anonymous'
		},
	],
	script: [
		{
			src: 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js',
			integrity: "sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN",
			crossorigin: "anonymous",
		}, {
			src: "https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js",
			integrity: "sha384-oBqDVmMz9ATKxIep9tiCxS/Z9fNfEXiDAYTujMAeBAsjFuCZSmKbSSUnQlmh/jp3",
			crossorigin: "anonymous"
		}
	],
})
</script>


