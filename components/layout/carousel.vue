<template>
    <div id="carousel" class="carousel slide show-menu-margin" data-bs-ride="true">
        <div class="carousel-indicators d-none d-md-flex">
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="0" class="active" aria-current="true"
                aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="3" aria-label="Slide 4"></button>
        </div>
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="../../assets/images/slide-8.png" class="d-block w-100" alt="Pessoa analisando items de credito">
                <div class="carousel-caption text-start">
                    <p class="mb-0 text-carousel"> Relatório de Crédito </p>
                    <ul class="mb-1">
                            <li>
                                Restrição Comercial
                            </li>
                            <li>
                                Pendencia financeira
                            </li>
                            <li>
                                Protesto Nacional
                            </li>
                    </ul>
                    <button class="btn btn-outline-primary rounded-pill btn-blue-primary fw-light text-white"> Saiba mais </button>
                </div>
            </div>
            <div class="carousel-item">
                <img src="../../assets/images/slide-7.png" class="d-block w-100"
                    alt="Pessoa escrevendo e calculando alguma conta">
            </div>
            <div class="carousel-item">
                <img src="../../assets/images/slide-6.png" class="d-block w-100" alt="Pessoa com a mão no volante">
            </div>
            <div class="carousel-item">
                <img src="../../assets/images/slide-5.png" class="d-block w-100" alt="Pessoa entrando em um carro">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>


<style>
.btn-blue-primary {
    background-color: var(--color-primary-3);
    transition: 0.3s;
    letter-spacing: 0.2px;
}

.text-carousel {
    font-size: x-large;
}

.show-menu-margin {
    margin-top: 8rem;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
    .text-carousel {
        font-size: medium;
    }
}

@media only screen and (min-width: 992px) {
    .show-menu-margin {
        margin-top: 0;
    }
}

</style>