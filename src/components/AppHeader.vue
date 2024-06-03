<script>
export default {
    data() {
        return {
            links: ['Tutte', 'Acquista di nuovo', ' Cronologia di navigazione', 'Amazon Business', 'Offerte', 'Amazon.it di Luca', 'Buoni Regalo', 'eBook in Italiano'],
            logo: 'logo-header.png',
            navLinks: [
                {
                    first: 'Ciao',
                    second: 'Account e liste'
                },
                {
                    first: 'Resi',
                    second: 'e ordini'
                },
                {
                    first: null,
                    second: 'Carrello'
                },
            ]
        };
    },
    methods: {
        getImageUrl(logo) {
            return new URL('../img/' + logo, import.meta.url).href;
        }
    },
}
</script>

<!-- DA POPOLARE DINAMICAMENTE  -->
<template>
   <header>
    <div class="ms-header-top">
        <div class="d-flex justify-content-between align-items-center">
            <div class="ms-header-left ms-2">
                <img :src="getImageUrl(logo)" alt="">
            </div>
            <div class="center mt-1">
                <div class="input-group mb-3">
                    <button class="btn btn-outline-secondary dropdown-toggle input-color" type="button" data-bs-toggle="dropdown" aria-expanded="false">Tutte le categorie</button>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Action</a></li>
                        <li><a class="dropdown-item" href="#">Another action</a></li>
                        <li><a class="dropdown-item" href="#">Something else here</a></li>
                        <li><hr class="dropdown-divider"></li>
                        <li><a class="dropdown-item" href="#">Separated link</a></li>
                    </ul>
                    <input type="text" class="form-control" aria-label="Text input with dropdown button">
                </div>
            </div>
            <div class="right d-flex px-1 text-white" v-for="navLink in navLinks">
                <div>
                    <div>{{ navLink.first }}</div>
                    <div v-if="!navLink.first"><i class="fa-solid fa-cart-shopping"></i></div>
                    <div><strong>{{ navLink.second }}</strong></div>
                </div>

            </div>
      </div>
    </div>

    <!-- <div class="ms-header-bottom mt-0">
            <div class="d-flex justify-content-between">
                <div class="left-bot d-flex align-items-center p-0 m-0">
                    <div class="ms-nav">
                        <ul class="list-unstyled d-flex gap-3" >
                            <li v-for="link in links" class="">
                                <a href="">{{ link }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="right-bot me-2">
                    <p>Festa della mamma: rendi il suo giorno speciale</p>
                </div>
            </div>
    </div> -->

    <div class="ms-header-bottom d-flex align-items-center justify-content-between">
        <div class="ms-header-bottom-left">
            <nav class="navbar ms-navbar navbar-expand-lg">
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="nav me-auto mb-2 mb-lg-0 list-unstyled" >
                        <li v-for="link in links" class="nav-item ms-nav-item">
                            <a class="nav-link px-2 text-white ms-fs" href="">{{ link }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>

        <div class="ms-header-bottom-right me-2 ms-fs">
            <div class="text-white">Festa della mamma:<span class="ms-text-gray"> rendi il suo giorno speciale</span></div>
        </div>

    </div>


   </header>
</template>

<style scoped lang="scss">

@use '../style/partials/variables' as *;



.ms-header-top {
    background-color: $brand_primary;

    .ms-header-left {
        height: 40px;

        img {
            height: 100%;
        }
    }
}

.ms-header-bottom {
    width: 100%;
    background-color: $brand_primary_light;

    .ms-fs {
        font-size: 14px;
    }

    .ms-navbar {
        max-height: 40px;
    }

    .ms-text-gray {
        color: $brand_secondary_dark;
    }

}



</style>