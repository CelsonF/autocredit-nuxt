<script lang="ts">
import { defineComponent, onMounted, reactive, toRefs  } from "vue"
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
			bgColor : '',
			textColors : '',
			imgLogo : true,
			typeMenu:'',
			toggleMenu:''
		})
	
		const scrollPage = (() => {
			if(window.scrollY === 0 && window.outerWidth > 992) {
				state.bgColor = "bg-transparent",
				state.imgLogo = false,
				state.typeMenu = "fixed-top"
				state.textColors = 'text-white'
				state.toggleMenu = 'text-white'
			} else {
				state.bgColor = "bg-light shadow-sm filter-glassmorfism",
				state.textColors = "text-black",
				state.toggleMenu = "text-black"
				state.imgLogo = true
			}
		})

		const getScrollY = (() => {
			window.addEventListener('scroll', scrollPage)
		})

		const windowWitdhScreen = (() => {
			if(window.outerWidth < 992 && window.scrollY === 0) {
				state.bgColor = "bg-light shadow-sm filter-glassmorfism",
				state.textColors = "text-black",
				state.toggleMenu = "text-black"
				state.imgLogo = true
			}
		})
		

		onMounted(() => {	
			state.imgLogo = false
			state.textColors = 'text-white'
			state.toggleMenu = 'text-white'
			state.typeMenu = "fixed-top"
			getScrollY()
			windowWitdhScreen()
		})

		return { ...toRefs(state),scrollPage,getScrollY,windowWitdhScreen}
	},
})

</script>

<template>
	<header :class="typeMenu">
		<Navbar :bg-menu="bgColor" :text-colors="textColors"  :img-logo="imgLogo" :toggle-menu="toggleMenu"/>
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
