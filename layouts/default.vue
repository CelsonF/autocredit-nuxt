<script setup lang="ts">
import Navbar from "~/components/layout/navbar.vue"

const emailWebsite = 'autocreditconsultas@gmail.com'
const phoneNumber = '(31)97362-0350'


</script>

<template>
	<header class="sticky-top">
		<Navbar />
	</header>
	<slot />
	<footer class="container-fluid bg-light">
		<div class="container">
			<div class="pt-5 pb-2">
				<div class="row justify-content-between">
					<div class="col-6 col-md-2 mb-3">
						<h5>Contato</h5>
						<ul class="nav flex-column">
							<li class="nav-item mb-2">
								<a href="#" class="nav-link p-0 text-muted">
									Número:
								</a>
							</li>
							<li class="nav-item mb-2">{{ phoneNumber }}</li>

						</ul>
					</div>

					<div class="col-md-5 offset-md-1 mb-3 align-self-center">
						<form>
							<h5>Entre em contato atráves do nosso email:</h5>
							<p>{{ emailWebsite }}</p>
						</form>
					</div>
				</div>
				<div class="d-flex flex-column flex-sm-row justify-content-between py-4 my-4 border-top">
					<p>© 2022 Autocredit . Todos os direitos reservados.</p>
				</div>
			</div>
		</div>
	</footer>
</template>
