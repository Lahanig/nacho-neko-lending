<template>
    <section class="mt-5 wiki">
        <div class="container">
            <div class="wiki-inner">

                <div class="wiki-inner-header">
                    <span>Name card</span>
                </div>

                <div class="wiki-inner-body mt-3">
                    <div class="wiki-inner-body-text-section" id="s-1">
                        <span>
                            Nachoneko (なちょ猫); also known by her real name Amashiro Natsuki (甘城なつき) is a female independent Japanese Virtual YouTuber and illustrator. <br><br>
                            She joined Twitter in November 2013 and her YouTube channel was created on 19 July 2014. Prior to becoming a VTuber, Nacho did occasional streams on her Twitch channel.<br><br>
                            Nacho officially confirmed her plans to debut as a VTuber on 15 June 2021 in a tweet in which she showed off her full VTuber model.
                        </span>
                    </div>

                    <div class="wiki-inner-body-text-section" id="s-2">
                        <div class="wiki-inner-body-text-section-img">
                            <img src="../../assets/imgs/name-card.webp" draggable="false">
                        </div>
                        
                        <div class="wiki-inner-body-text-section-title mt-4">Nachoneko</div>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>

<style scoped>
.wiki {
    width: 100%;
}

.wiki-inner {
    display: flex;
    flex-direction: column;

    width: 100%;
}

.wiki-inner-header {
    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 6px;

    background-color: var(--primary-color);
}

.wiki-inner-header span {
    font-size: 1.6em;

    color: #eee;
}

.wiki-inner-body {
    display: flex;
    flex-direction: column;

    padding: 1.5rem;
}

.wiki-inner-body-text-section {
    display: flex;
    justify-content: center;

    font-size: 1.4em;

    width: 100%;
    max-width: auto;
}

.wiki-inner-body #s-1 {
    width: 100%;

    padding-right: 1rem;
}

.wiki-inner-body #s-2 {
    width: 100%;

    margin-top: 1.5rem;

    flex-direction: column;
    justify-content: center;

    margin-left: none;
}

.wiki-inner-body-text-section-img {
    display: flex;
    justify-content: center;

    width: 100%;
}

.wiki-inner-body-text-section-img img{
    width: 100%;
}

.wiki-inner-body-text-section-title {
    display: flex;
    justify-content: center;

    border-radius: 3px;

    color: #eee;
    background-color: var(--primary-color);
}

@media (min-width: 1024px) {
    .wiki-inner-body {
        flex-direction: row;
    }

    .wiki-inner-body #s-1 {
        padding-right: 1rem;
    }

    .wiki-inner-body #s-2 {
        margin-top: 0rem;

        margin-left: auto;
    }

    .wiki-inner-body-text-section {
        width: 50%;
        max-width: 550px;
    }
}
</style>