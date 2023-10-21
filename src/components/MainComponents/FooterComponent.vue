<template>
    <footer class="footer mt-5">
        <div class="footer-inner">
            <div class="footer-inner-body">

                <div class="footer-inner-body" id="s-1">
                    <span><a href="https://virtualyoutuber.fandom.com/wiki/Nachoneko" target="_blank">virtualyoutuber.fandom.com/wiki/Nachoneko</a></span>
                    <span><a href="https://twitter.com/amsrntk3" target="_blank">@amsrntk3</a></span>
                </div>

                <div class="footer-inner-body mobile" id="s-2">
                    <span>©Nacho's site</span>
                </div>

                <div class="footer-inner-body desktop" id="s-2">
                    <span>©Nacho's site</span>
                </div>

            </div>
        </div>
    </footer>
</template>

<style scoped>
    footer {
        width: 100%;
    }

    .footer-inner {
        display: flex;

        border: 1px solid var(--primary-color);

        width: 100%;
    }

    .footer-inner::before {
        display: flex;
        justify-content: center;

        position: absolute;

        color: #eee;

        margin-top: -30px;
        margin-left: calc(1rem + 3vw);

        content: 'Links to sources';

        background-color: var(--primary-color);

        border-radius: 25px 25px 0 0px;

        padding: .1em 2em;

        font-size: 1.1em;
    }

    .footer-inner-body {
        display: flex;
        flex-wrap: wrap;

        width: 100%;

        font-size: 1.08em;
    }

    .footer-inner-body #s-1 {
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;

        width: 100%;

        padding: 1rem 2rem 0 2rem;
    }

    .footer-inner-body #s-2 {
        display: flex;
        align-items: center;
        flex-wrap: wrap;

        width: 100%;

        padding: 0rem 2rem .3rem 2rem;

        border-radius: 0 0 0 100px;

        color: #eee;

        background-color: var(--primary-color);
    }

    .desktop {
        display: none!important;
    }

    .mobile {
        display: flex!important;

        background-color: transparent!important;
        color: var(--primary-color)!important;
    }

    .footer-inner-body #s-1 span {
        color: var(--primary-color);
        max-width: calc(100% - 1rem);

        text-overflow: ellipsis;

        overflow: hidden;
    }

    .footer-inner-body #s-2 span {
        margin-left: auto;
    }

    @media (min-width: 1024px) {
        .desktop {
            display: flex!important;
        }

        .mobile {
            display: none!important;
        }

        .footer-inner-body #s-1 {
            width: 50%;

            padding: .5rem 2rem;
        }

        .footer-inner-body #s-2 {
            width: 50%;

            padding: .5rem 2rem;
        }
    }
</style>