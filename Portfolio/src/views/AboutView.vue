<template>
    <div class="about-page__wrapper">
        <div class="about-page__content">
            <div class="about-page__img__wrapper ">
                <img src="../assets/images/me.png" class="about-page__content__img">
            </div>
            <div class="about-page__content__text">
                <div class="about-page__content__text__heading">
                    <p class="about-page__content__text__heading__one">About</p>
                    <p class="about-page__content__text__heading__two">Maria <b>Durrani</b></p>

                </div>
                <div class="about-page__content__text__paragraph">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iusto dicta reprehenderit aliquam
                        dolor
                        sunt minus minima ut porro sed ex rem laudantium eos, ratione quos molestiae ullam tempora atque
                        numquam. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Possimus libero in alias,
                        fuga
                        veritatis, nemo error autem, quos rem maxime blanditiis reprehenderit laudantium neque
                        temporibus?
                        Ipsa tempore molestiae nulla ipsam.
                    </p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatem amet corporis non incidunt?
                        Libero sunt dolorem, temporibus autem explicabo deserunt, iure unde natus quod sint ex ullam hic
                        adipisci mollitia! Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolore architecto
                        aut molestiae, itaque explicabo harum! Non sit ipsam omnis, ex doloribus vero commodi tempore
                        magnam odio dolorem, totam nisi natus.</p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatem amet corporis non incidunt?
                        Libero sunt dolorem, temporibus autem explicabo deserunt, iure unde natus quod sint ex ullam hic
                        adipisci mollitia! Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolore architecto
                        aut molestiae, itaque explicabo harum! Non sit ipsam omnis, ex doloribus vero commodi tempore
                        magnam odio dolorem, totam nisi natus.</p>
                </div>

                <div class="about-page__content__cv-button">
                    <a href="">My CV</a>
                </div>
            </div>


        </div>
    </div>
</template>

<style src="../assets/AboutView.scss"></style>

<script>
export default {
    mounted() {
        const about = document.querySelector(".about-page__content__text__paragraph");

        about?.addEventListener("click", e => {
            console.log(e);
        });
    }
}
</script>