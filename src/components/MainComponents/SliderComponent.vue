<template>
    <section class="slider mt-4">
        <div class="container">
            <div class="slider-inner">

                <div class="slider-inner-header wow slideInLeft" data-wow-duration="1s" data-wow-delay=".0s" data-wow-offset="200" data-wow-iteration="1">
                    Gallery
                </div>

                <div class="slider-inner-body wow wow slideInRight" data-wow-duration="1s" data-wow-delay=".0s" data-wow-offset="200" data-wow-iteration="1">
                    <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="true">
                        <div class="carousel-indicators">
                            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
                            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
                        </div>
                        <div class="carousel-inner">
                            <div class="carousel-item active" data-bs-interval="3000">
                                <img src="../../assets/imgs/gallery-item-1.webp" class="d-block w-100" alt="gallery-item-1" draggable="false">
                            </div>
                            
                            <div class="carousel-item" data-bs-interval="3000">
                                <img src="../../assets/imgs/gallery-item-2.jpg" class="d-block w-100" alt="gallery-item-2" draggable="false">
                            </div>
                            
                            <div class="carousel-item" data-bs-interval="3000">
                                <img src="../../assets/imgs/gallery-item-3.jpeg" class="d-block w-100" alt="gallery-item-3" draggable="false">
                            </div>
                        </div>

                        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
                            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                            <span class="visually-hidden">Prev</span>
                        </button>

                        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
                            <span class="carousel-control-next-icon" aria-hidden="true"></span>
                            <span class="visually-hidden">Next</span>
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>

<style scoped>
.slider {
    width: 100%;
}

.slider-inner {
    display: flex;
    flex-direction: column;

    width: 100%;
}

.slider-inner-header {
    display: flex;
    justify-content: center;

    color: #eee;

    font-size: 1.6em;

    border-radius: 3px 3px 0px 0px;

    background-color: var(--primary-color);
}

.slider-inner-body {
    display: flex;
    flex-direction: column;
}

.slider-inner-body img {
    object-fit: cover;
    max-height: 706px;
}
</style>