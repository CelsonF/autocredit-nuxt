<script lang="ts">
import { defineComponent, onMounted, ref } from 'vue';
import serviceItems from '../static/itemsServices.json'

export default defineComponent({
	setup() {
		const services = ref();



		onMounted(() => {
			services.value = serviceItems.contents;
		});

		return {
			services
		};
	},
});

</script>


<template>
	<section class="container-fluid low-opacity-bg-image pb-5" id="servico">
		<h1 class="text-white text-center pt-4">Nossos Produtos</h1>

		<div class="container">
			<div class="row">
				<div class="col-12 col-md-4 col-lg-3 mt-5" v-for="item in services" :key="item.id">
					<div data-bs-toggle="modal" data-bs-target="#modalService"
						class="card rounded-5 min-h animate-card shadow-sm align-items-center"
						@click="$emit('modalExibition', item)">
						<h5 class="card-title py-3 px-2 ">{{ item.title }}</h5>
						<div class="card-body d-flex align-items-center pt-0">
							<div class="icons-service d-flex justify-content-center align-items-center">
								<img :src="'/icons/' + item.icon" :alt="item.title" class="icons-witdh-service" />
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>


<style scoped>
.icons-service {
	width: 6.25rem;
	height: 6.25rem;

	border-radius: 50%;

	background-color: var(--color-primary-3);
}

.icons-witdh-service {
	width: 4rem;
}

.min-h {
	min-height: 15rem;
}

.animate-card {
	transition: 0.5s;
}

.animate-card:hover {
	transition: 0.5s;
	cursor: pointer;
	transform: translateY(-0.34rem);
}

.low-opacity-bg-image {
	--bg-image: url("../assets/images/business-man-fullhd.jpg");
	--bg-image-opacity: 0.25;

	background-color: #1c1c1c;

	position: relative;

	isolation: isolate;
}

.low-opacity-bg-image::after {
	content: "";
	position: absolute;
	z-index: -1;
	inset: 0;

	opacity: var(--bg-image-opacity);


	background-image: var(--bg-image);
	background-size: cover;
	background-position: center;
}
</style>
