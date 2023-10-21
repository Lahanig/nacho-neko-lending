<template>
    <section class="trivia mt-5" name="trivia">
        <div class="container">
            <div class="trivia-inner">

                <div class="trivia-inner-header wow fadeInDown" data-wow-duration="1s" data-wow-delay=".0s" data-wow-offset="300" data-wow-iteration="1">
                    <span>Trivia</span>
                </div>

                <div class="trivia-inner-body mt-2 wow fadeInLeft" data-wow-duration="1s" data-wow-delay=".0s" data-wow-offset="200" data-wow-iteration="1">
                    <span>
                        <ul>
                            <li>Before becoming a VTuber herself, Nacho created character designs for other VTubers such as Gawr Gura, Araka Luto and Draki Kona, and redesigned VTubers such as Kamiko Kana and Gokigen Naname. She also created the character design for an independent VTuber, Karubi Akami.</li>
                        </ul>
                    </span>
                </div>

            </div>
        </div>
    </section>
</template>

<style scoped>
    .trivia {
        width: 100%;
    }

    .trivia-inner {
        width: 100%;

        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .trivia-inner-header {
        display: flex;
        justify-content: center;

        font-size: 2em;

        color: #eee;

        border-radius: 3px;

        background-color: var(--primary-color);
    }

    .trivia-inner-body {
        display: flex;
        justify-content: center;

        font-size: 1.5em;

        width: 100%;
    }

    .trivia-inner-body span {
        max-width: 100%;
    }
</style>