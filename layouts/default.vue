<script setup lang="ts">
import Navbar from "~/components/layout/navbar.vue"
</script>

<template>
	<header class="sticky-top">
		<Navbar />
	</header>
	<slot />
</template>
