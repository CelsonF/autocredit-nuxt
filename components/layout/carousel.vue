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
                    <div class="mb-0 fs-title"> Relatório de Crédito </div>
                    <ul class="mb-1 list-caption ps-0">
                            <li class="list-items">
                                Restrição Comercial
                            </li>
                            <li class="list-items">
                                Pendencia financeira
                            </li>
                            <li class="list-items">
                                Protesto Nacional
                            </li>
                    </ul>
                </div>
            </div>
            <div class="carousel-item">
                <img src="../../assets/images/slide-7.png" class="d-block w-100"
                    alt="Pessoa escrevendo e calculando alguma conta">
                <div class="carousel-caption text-end">
                    <div class="mb-0 fs-title"> Ações Judiciais </div>
                    <ul class="mb-1 list-caption s-0">
                            <li class="list-items">
                                Antecedentes criminais
                            </li>
                            <li class="list-items">
                                Ações Trabalhista
                            </li>
                    </ul>
                </div>
            </div>
            <div class="carousel-item">
                <img src="../../assets/images/slide-6.png" class="d-block w-100" alt="Pessoa com a mão no volante">
                <div class="carousel-caption text-start">
                    <div class="mb-0 fs-title"> Consulta veicular </div>
                    <ul class="mb-1 list-caption ps-0">
                            <li class="list-items">
                                Leilão/sinistro
                            </li>
                            <li class="list-items">
                                Débitos e multas
                            </li>
                            <li class="list-items">
                                Histórico de roubo e furto
                            </li>
                            <li class="list-items">
                                Renainf
                            </li>
                    </ul>
                </div>
            </div>
            <div class="carousel-item">
                <img src="../../assets/images/slide-5.png" class="d-block w-100" alt="Pessoa entrando em um carro">
                <div class="carousel-caption text-end">
                    <div class="mb-0 fs-title"> Comunicado de Vendas </div>
                    <ul class="mb-1 list-caption s-0">
                            <li class="list-items">
                                ATPV-E
                            </li>
                            <li class="list-items">
                                CRLV
                            </li>
                    </ul>
                </div>
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

.fs-title{
        font-size: 1.2rem;
}
    
.list-items {
        font-size: 0.7rem;
}

.list-caption li {
    list-style-type: none;
    text-decoration: none;
}


/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
    .fs-title{
        font-size: 2rem;
    }
    
    .list-items {
        font-size: 1rem;
    }
}

@media only screen and (min-width: 992px) {
    .show-menu-margin {
        margin-top: 0;
    }

    .fs-title{
        font-size: 4rem;
    }
    
    .list-items {
        font-size: 2rem;
    }
}




</style>