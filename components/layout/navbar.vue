<template>
	<nav
		class="navbar navbar-expand-lg shadow-sm bg-body-tertiary navbar-light bg-light">
		<div
			class="container-fluid justify-content-between justify-content-lg-around">
			<a class="navbar-brand me-0" href="#">
				<img
					src="../../assets/images/autocredit-logo.png"
					alt="autocredit"
					width="160"
					height="100" />
			</a>
			<ul
				class="navbar-nav nav-masthead gap-4 d-none d-lg-flex"
				id="navbarNavExpand">
				<li class="nav-item">
					<a class="nav-link active" aria-current="page" href="#home">Home</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" href="#servico">Serviços</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" href="#sobre">Sobre</a>
				</li>
			</ul>
			<a
				href="http://portalksiconsultas.com/"
				target="_blank"
				class="btn btn-outline-primary rounded-pill btn-blue-primary fw-light d-none d-lg-flex text-white">
				<img src="../../assets/images/icons/icon-singin.svg" class="pe-2" width="24" height="24" alt="entrar" />
				Acessar
			</a>
			<button
				class="navbar-toggler"
				type="button"
				data-bs-toggle="collapse"
				data-bs-target="#navbarToggleExternalContent"
				aria-controls="navbarToggleExternalContent"
				aria-expanded="false"
				aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>
		</div>

		<div class="collapse navbar-collapse" id="navbarToggleExternalContent">
			<ul class="navbar-nav px-3 me-auto mb-2 mb-lg-0 d-lg-none">
				<li class="nav-item text-center">
					<a class="nav-link active" aria-current="page" href="#home">Home</a>
				</li>
				<li class="nav-item text-center">
					<a class="nav-link" href="#servico">Serviço</a>
				</li>
				<li class="nav-item text-center">
					<a class="nav-link" href="#sobre"> Sobre </a>
				</li>
				<li class="nav-item">
					<a href="http://consultas.autocredit.com.br/"
						target="_blank"
						class="nav-link btn btn-outline-primary rounded-lg btn-blue-primary fw-light text-white">
						<img src="../../assets/images/icons/icon-singin.svg" class="pe-2" width="24" height="24" alt="entrar" />
						Acessar
					</a>
				</li>
			</ul>
		</div>
	</nav>
</template>

<style>
.btn-blue-primary {
	background-color: var(--color-primary-3);
	transition: 0.3s;
	letter-spacing: 0.2px;
}

.btn-blue-primary:hover {
	background-color: var(--color-primary-4);
	transition: 0.3s;
}

.nav-masthead .nav-link {
	color: rgba(4, 4, 4, 0.5);
	border-bottom: 0.25rem solid transparent;
}

.nav-masthead .nav-link:hover,
.nav-masthead .nav-link:focus {
	border-bottom-color: rgba(4, 4, 4, 0.25);
}

.nav-masthead .nav-link+.nav-link {
	margin-left: 1rem;
}

.nav-masthead .active {
	color: rgb(74, 128, 254);
	border-bottom-color: rgb(36, 131, 255);
}
</style>
