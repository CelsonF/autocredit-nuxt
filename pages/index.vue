<script  lang="ts">
import {defineComponent,reactive,toRefs} from "vue"
import Servicos from "~/pages/servicos.vue"
import Carousel from "~/components/layout/carousel.vue"
import Modal from "~/components/layout/modal.vue"

export default defineComponent({
	components: {
		Servicos,
		Carousel,
		Modal
	},
	setup() {
		const state = reactive({
			contentItem: {}
		})

		const modalDialog = ((content:Object) =>{
			state.contentItem = content
		})

		return {
			...toRefs(state),modalDialog
		}
	}
})

</script>

<template>
	<main>
		<Carousel />

		<section class="container-xl py-5">
			<h1 class="text-center py-5">
				Como são as consultas da Autocredit ?
			</h1>
			<div class="row pt-4 pb-3">
				<div class="col-12 col-md-4">
					<div class="d-flex flex-column align-items-center">
						<div class="icons d-flex justify-content-center align-items-center">
							<img class="img-fluid" src="../assets/images/icons/svg_24h-4.svg" alt="consultas 24 por 7" />
						</div>
						<div class="text-center px-4">
							<h3 class="fw-bold py-3 m-0">Consultas 24/7</h3>
							<p class="px-2 py-3">
								Consultas em tempo real , com a disponibilidade 24h por dia e 7
								dias por semana.
							</p>
						</div>
					</div>
				</div>
				<div class="col-12 col-md-4">
					<div class="d-flex flex-column align-items-center">
						<div class="icons d-flex justify-content-center align-items-center">
							<img class="img-fluid" src="../assets/images/icons/svg_facil_utilizacao-4.svg"
								alt="Consultas fácil e confiável" />
						</div>
						<div class="text-center px-4">
							<h3 class="fw-bold py-3 m-0">Fácil e Confiável</h3>
							<p class="px-2 py-3">
								Consultas objetivas, trazendo dados autalizados e 100%
								confiáveis.
							</p>
						</div>
					</div>
				</div>
				<div class="col-12 col-md-4">
					<div class="d-flex flex-column align-items-center">
						<div class="icons d-flex justify-content-center align-items-center">
							<img class="img-fluid" src="../assets/images/icons/svg_preco_acessivel-4.svg"
								alt="Preços acessíveis" />
						</div>
						<div class="text-center px-4">
							<h3 class="fw-bold py-3 m-0">Preço Acessível</h3>
							<p class="px-2 py-3">
								Consultas com preço acessíveis em relação aos seus concorrentes.
							</p>
						</div>
					</div>
				</div>
			</div>
		</section>

		<Servicos @modal-exibition="modalDialog"/>

		<section class="container-fluid d-flex low-bg-image-about flex-column justify-content-center pt-5 "
			id="sobre">
			<h1 class="py-2 text-center text-light mb-5"> Sobre </h1>
			<div class="container d-flex vh-lg-60">
				<div class="row flex-md-column flex-lg-row align-items-center">
					<div class="col-12 col-md-12 fs-5">
						<p class="text-center fs-5 fs-sm-3 text-light "> 
							A Autocredit é uma empresa altamente especializada e confiável que se destaca no mercado de consultas veiculares e análise de crédito. Com um compromisso inabalável com a satisfação do cliente, a empresa se esforça continuamente para atender às diversas necessidades de seus clientes de maneira excepcional. Sua abordagem focada em oferecer consultas atualizadas, seguras e confiáveis estabelece um padrão elevado no setor.
Uma das características distintivas da Autocredit é a sua ampla e sólida base de dados. Essa base de dados é o alicerce que permite à empresa fornecer informações detalhadas e precisas sobre veículos e dados de crédito. A robustez e a segurança dessa base de dados asseguram que os clientes possam confiar nas informações e análises apresentadas, tornando a Autocredit uma escolha confiável para quem busca informações confiáveis no campo automotivo e financeiro.
						</p>
					</div>
					<!-- <div class="col-12 col-md-6">
						<img class="img-fluid" src="../assets/images/car_blue.png" alt="carro azul">
					</div> -->
				</div>
			</div>
		</section>

		<div class="whatsapp-button fixed-bottom d-flex justify-content-end me-2 mb-2 me-lg-3 mb-lg-3">
			<a aria-label="Chat on WhatsApp" target="_blank"
				href="https://wa.me/5531973620350?text=Gostaria%20de%20saber%20mais%20sobre%20a%20Autocredit."
				class="rounded-circle box-whatsapp">
				<img class="img-fluid icon-whatsapp" src="../assets/images/icons/whatsapp-autocredit.svg"
					alt="Icone de whats app flutuante ">
			</a>
		</div>

		<Modal :content="contentItem" />
	</main>
</template>



<style scoped>
.vh-lg-60 {
	min-height: 70vh;
}

.icons {
	width: 6.25rem;
	height: 6.25rem;

	border-radius: 50%;

	background-color: var(--color-primary-1);
}



.icon-whatsapp {
	width: 2.5rem;
	height: 2.5em;


	background-color: transparent;
}

.box-whatsapp {
	transform: scale(0.9);
	transition: 0.3s;
}

.box-whatsapp:hover {
	background-color: #dedede;
	padding: 0.7rem;
	transform: scale(1);
	transition: 0.3s;
	box-shadow: inset 0px 1px 5px #141132;
}



.low-bg-image-about {
	/* --bg-image: url("../assets/images/bg-squares.svg");
	--bg-image-second: url("../assets/images/blue-triangles.svg"); */
	--bg-image-opacity-about: 0.25;

	background-color: #202020;

	background-repeat: no-repeat;

	position: relative;

	isolation: isolate;
}


.low-bg-image-about::after {
	content: "";
	position: absolute;
	z-index: -1;
	inset: 0;

	opacity: var(--bg-image-opacity-about);

	background-repeat: no-repeat;
	background-image: var(--bg-image), var(--bg-image-second);
	background-size: contain;
	background-position: left, right;
}



/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
	.icon-whatsapp {
		width: 3rem;
		height: 3rem;
	}
}
</style>
