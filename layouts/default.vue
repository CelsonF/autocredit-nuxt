<script lang="ts">
import { defineComponent, onMounted, reactive, toRefs ,ref } from "vue"
import Navbar from "~/components/layout/navbar.vue"
import Slide from "~/components/layout/slide.vue"

export default defineComponent({
	components: {
		Navbar,
		Slide,
	},
	setup() {
		const state = reactive({
			emailWebsite:'autocreditconsultas@gmail.com',
			phoneNumber:'(31)97362-0350',
		})
		const bgColor = ref('');
		const textColors = ref('');
		const imgLogo = ref(true);

		const scrollPage = (() => {
			console.log("Algo foi montado")
			if(window.scrollY === 0) {
				bgColor.value = "bg-transparent",
				textColors.value = "text-white",
				imgLogo.value = true
			} else {
				bgColor.value = "bg-light shadow-sm filter-glassmorfism",
				textColors.value = "text-black",
				imgLogo.value = false
			}
		})

		const getScrollY = (() => {
			window.addEventListener('scroll', scrollPage)
		})

		onMounted(() => {	
			textColors.value = "text-white"
			getScrollY()
		})

		return { ...toRefs(state),bgColor,textColors,imgLogo,scrollPage,getScrollY}
	},
})

</script>

<template>
	<header class="fixed-top">
		<Navbar :bg-menu="bgColor" :text-colors="textColors"  :img-logo="imgLogo"/>
	</header>
	<slot />
	<Slide />
	<footer class="container-fluid bg-light">
		<div class="container">
			<div class="pt-5 pb-2">
				<div class="row justify-content-between">
					<div class="col-md-5 mb-3 align-self-center">
						<form>
							<h5>Entre em contato conosco:</h5>
							<p>
								<a class="no-style"
									href="mailto:autocreditconsultas@gmail.com.br?subject=Contato da Autocredit&body=Seja bem vindo a autocredit escreva o motivo do seu contato abaixo.">
									<img class="icons-footer" src="../assets/images/icons/email-icon.svg"
										alt="autocreditconsultas@gmail.com">
									{{ emailWebsite }}
								</a>
							</p>
							<p>
								<a class="no-style" href="tel:31 97362-0350">
									<img class="icons-footer" src="../assets/images/icons/telefone-autocredit.svg"
										alt="autocreditconsultas@gmail.com">
									{{ phoneNumber }}
								</a>
							</p>
						</form>
					</div>
					<div class="col-6 col-md-2 mb-3">
						<ul class="list-unstyled"> <span class="fw-semibold">Mapa do Site</span>
							<li><a class="no-style" href="#home">Home</a></li>
							<li><a class="no-style" href="#servico">Serviços</a></li>
							<li><a class="no-style" href="#sobre">Sobre</a></li>
						</ul>
					</div>
				</div>

				<div class="d-flex flex-column flex-sm-row justify-content-between py-4 my-4 border-top">
					<p>© 2022 Autocredit . Todos os direitos reservados.</p>
				</div>
			</div>
		</div>
	</footer>
</template>


<style>
.icons-footer {
	width: 1.1rem;
}

.no-style {
	text-decoration: none;
	color: #444;
}
</style>
