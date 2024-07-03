<template>
    <div class="contact-page__wrapper">

        <div class="contact-page__content-area">

            <p class="contact-page__headline">Contact</p>
            <hr class="contact-page__seperator">
            <div class="contact-page__options">

                <div class="contact-page__email">
                    <p class="contact-page__email__text">E-mail</p>
                    <a href="mailto:maria_durrani@hotmail.com"
                        class="contact-page__email__link">maria_durrani@hotmail.com</a>
                </div>

                <div class="contact-page__social-media">

                    <p class="contact-page__social-media__text">Social Media</p>
                    <ul class="contact-page__social-media__links">
                        <li><a href="https://www.linkedin.com/in/maria-durrani00/"
                                class="contact-page__linkedin">LinkedIn</a></li>
                        <li><a href="https://github.com/mariadurrani" class="contact-page__github">GitHub</a></li>
                    </ul>

                </div>

            </div>
        </div>

        <div class="contact-page__form-container">

            <div class="contact-page__form-text">
                <h2 class="contact-page__form-headline">Contact Me</h2>
                <p class="contact-page__form-p">I would love to hear from you</p> <!-- Change class -->
            </div>

            <form @submit.prevent="handleSubmit" class="contact-page__form">
                <p class="contact-page__form__send-message-p">Send me an Email</p>
                <ul class="contact-page__input">
                    <li> <input type="text" class="contact-page__input__name" placeholder="Name:" v-model="form.name" />
                        <span v-if="errors.name">{{ errors.name }}</span>
                    </li>
                    <li> <input type="email" class="contact-page__input__email" placeholder="Email:"
                            v-model="form.email" />
                        <span v-if="errors.email">{{ errors.email }}</span>
                    </li>
                    <li> <textarea class="contact-page__input__message" placeholder="Message:"
                            v-model="form.message"></textarea>
                        <span v-if="errors.message">{{ errors.message }}</span>
                    </li>
                </ul>

                <button type="submit" class="contact-page__submit-button">Submit</button>
            </form>

        </div>
    </div>


</template>

<style src="../assets/ContactView.scss"></style>

<script>
import { reactive } from 'vue';

export default {
    setup() {
        const form = reactive({
            name: '',
            email: '',
            message: ''
        });

        const errors = reactive({
            name: '',
            email: '',
            message: ''
        });

        const validateForm = () => {
            errors.name = form.name ? '' : 'Name is required';
            errors.email = form.email ? '' : 'Email is required';
            errors.message = form.message ? '' : 'Message is required';

            return !errors.name && !errors.email && !errors.message;
        }

        const handleSubmit = () => {
            if (validateForm()) {
                console.log('Form submitted:', form);
            } else {
                console.log("Some fields are not filled out correctly")

            }
        };

        return {
            form,
            errors,
            handleSubmit
        };
    }
};
</script>
