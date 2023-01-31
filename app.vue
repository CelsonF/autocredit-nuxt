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
    titleTemplate: ' Autocredit | %s',
    htmlAttrs: {
        lang: 'pt-BR'
    },
    meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
            hid: 'description',
            name: 'description',
            content: 'A Autocredit é uma empresa que atua no mercado de consulta veicular e análise de credito, sempre trabalhando para satisfazer as necessidades de seus clientes, trazendo consultas atualizadas, segura e confiável, contando com uma vasta base de dodos robusta e segura.'
        },
        { name: 'format-detection', content: 'telephone=no' },

      //Open Graph
    {
        hid: 'og:site_name',
        name: 'og:site_name',
        content: 'Autocredit'
    },
    {
        hid: 'og:type',
        name: 'og:type',
        content: 'website'
    },
    {
        hid: 'og:url',
        name: 'og:url',
        content: 'https://autocredit.com.br/'
    },
    {
        hid: 'og:title',
        name: 'og:title',
        content: 'Autocredit'
    },
    {
        hid: 'og:description',
        name: 'og:description',
        content: 'Autocredit a sua empresa de consulta veicular e análise de crédito.'
    },
    {
        hid: 'og:image',
        name: 'og:image',
        content: 'assets/images/autocredit-logo.png'
    },
	{
		property:'og:image:width',
		content:'160'
	},
	{
		property:'og:image:height',
		content:'100'
	},
	{
        hid: 'og:image',
        name: 'og:image',
        content: 'assets/images/icons/svg_24h-4.svg'
    },
	{
		property:'og:image:width',
		content:'80'
	},
	{
		property:'og:image:height',
		content:'80'
	},
	{
        hid: 'og:author',
        name: 'og:author',
        content: 'Time da Autocredit'
	}
    ],
    link: [
    {
        hid: 'canonical',
        rel: 'canonical',
        href: 'https://autocredit.com.br',
    },
    { 
		rel: 'icon',
		type: 'image/x-icon',
		href: 'assets/favicons/favicon.ico'
    },
    {
        rel: 'stylesheet',
        href: 'https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;500;700;800&display=swap'
    },
    {
        href: 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css',
        rel: 'stylesheet',
        integrity: 'sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD',
        crossorigin: 'anonymous',
    }
    ],
    script: [
    {
        src: 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js',
        integrity: 'sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN',
        crossorigin: 'anonymous'
    }
    ]
})
</script>


