<script>
export default {
    data() {
        return {
            links: ['Tutte', 'Acquista di nuovo', ' Cronologia di navigazione', 'Amazon Business', 'Offerte', 'Amazon.it di Luca', 'Buoni Regalo', 'eBook in Italiano']
        };
    }
}
</script>
<!-- DA POPOLARE DINAMICAMENTE  -->
<template>
   <header>
    <div class="top">
        <div class="d-flex justify-content-between px-2 align-items-center">
            <div class="left">amazon</div>
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
            <div class="right d-flex gap-3">
                <div>ok</div>
                <div>ok</div>
                <div>ok</div>
            </div>
      </div>
    </div>

    <div class="bottom mt-0">
            <div class="d-flex justify-content-between">
                <div class="left-bot">
                    <div class="ms-nav d-flex ">
                        <ul class="list-unstyled px-2">
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="">ok</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="right-bot me-2">
                    <p>Festa della mamma: rendi il suo giorno speciale</p>
                </div>
            </div>
    </div>


   </header>
</template>

<style scoped lang="scss">
 @use '../style/partials/_variables' as *;
 .top{
    background-color: $brand_primary;
 }
 .bottom{
    background-color: $brand_primary_light;
    color:$brand_secondary;
 }

 .input-color{
    background-color: $brand_secondary_dark;
    color :$brand_secondary;
 }
 .left,.right
 {
    color: $brand_secondary;
 }
.center{
    width:80%
}
input{
    width: 100%;
}
li{
    list-style: none;
}
a{
    text-decoration: none;
    color: inherit;
}
</style>