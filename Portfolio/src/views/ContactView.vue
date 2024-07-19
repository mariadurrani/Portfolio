<template>
    <div class="contact-page__wrapper">

        <div class="contact-page__form-container">

            <div class="contact-page__form-text">
                <h2 class="contact-page__form-headline">Contact Me</h2>
                <p class="contact-page__form-p">I would love to hear from you</p> <!-- Change class -->
            </div>
            <div class="contact-page__content">
                <form @submit.prevent="handleSubmit" class="contact-page__form">
                    <p class="contact-page__form__send-message-p">Send me an Email</p>
                    <ul class="contact-page__input">
                        <li> <input type="text" class="contact-page__input__name" placeholder="Name:"
                                v-model="form.name" />
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

                <div>
                    <div class="contact-page__phone">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" width="60">
                            <path fill="#4f5051"
                                d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z" />
                        </svg>
                        <p class="contact-page__phone__text">Phone:</p>
                        <a href="tel:+46730226833" class="contact-page__phone__link">+46 730 226 833</a>
                    </div>

                    <div class="contact-page__email">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" width="60">
                            <path fill="#4f5051"
                                d="M256 64C150 64 64 150 64 256s86 192 192 192c17.7 0 32 14.3 32 32s-14.3 32-32 32C114.6 512 0 397.4 0 256S114.6 0 256 0S512 114.6 512 256v32c0 53-43 96-96 96c-29.3 0-55.6-13.2-73.2-33.9C320 371.1 289.5 384 256 384c-70.7 0-128-57.3-128-128s57.3-128 128-128c27.9 0 53.7 8.9 74.7 24.1c5.7-5 13.1-8.1 21.3-8.1c17.7 0 32 14.3 32 32v80 32c0 17.7 14.3 32 32 32s32-14.3 32-32V256c0-106-86-192-192-192zm64 192a64 64 0 1 0 -128 0 64 64 0 1 0 128 0z" />

                        </svg>
                        <p class="contact-page__email__text">E-mail:</p>
                        <a href="mailto:maria_durrani@hotmail.com"
                            class="contact-page__email__link">maria_durrani@hotmail.com</a>
                    </div>

                    <div class="contact-page__social-media">
                        <ul class="contact-page__social-media__links">
                            <li><a href="https://www.linkedin.com/in/maria-durrani00/"
                                    class="contact-page__linkedin"><svg xmlns="http://www.w3.org/2000/svg"
                                        viewBox="0 0 448 512" width="30">
                                        <path fill="#4f5051"
                                            d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z" />
                                    </svg></a></li>

                            <li><a href="https://github.com/mariadurrani" class="contact-page__github"><svg
                                        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" width="30">
                                        <path fill="#4f5051"
                                            d="M448 96c0-35.3-28.7-64-64-64H64C28.7 32 0 60.7 0 96V416c0 35.3 28.7 64 64 64H384c35.3 0 64-28.7 64-64V96zM265.8 407.7c0-1.8 0-6 .1-11.6c.1-11.4 .1-28.8 .1-43.7c0-15.6-5.2-25.5-11.3-30.7c37-4.1 76-9.2 76-73.1c0-18.2-6.5-27.3-17.1-39c1.7-4.3 7.4-22-1.7-45c-13.9-4.3-45.7 17.9-45.7 17.9c-13.2-3.7-27.5-5.6-41.6-5.6s-28.4 1.9-41.6 5.6c0 0-31.8-22.2-45.7-17.9c-9.1 22.9-3.5 40.6-1.7 45c-10.6 11.7-15.6 20.8-15.6 39c0 63.6 37.3 69 74.3 73.1c-4.8 4.3-9.1 11.7-10.6 22.3c-9.5 4.3-33.8 11.7-48.3-13.9c-9.1-15.8-25.5-17.1-25.5-17.1c-16.2-.2-1.1 10.2-1.1 10.2c10.8 5 18.4 24.2 18.4 24.2c9.7 29.7 56.1 19.7 56.1 19.7c0 9 .1 21.7 .1 30.6c0 4.8 .1 8.6 .1 10c0 4.3-3 9.5-11.5 8C106 393.6 59.8 330.8 59.8 257.4c0-91.8 70.2-161.5 162-161.5s166.2 69.7 166.2 161.5c.1 73.4-44.7 136.3-110.7 158.3c-8.4 1.5-11.5-3.7-11.5-8zm-90.5-54.8c-.2-1.5 1.1-2.8 3-3.2c1.9-.2 3.7 .6 3.9 1.9c.3 1.3-1 2.6-3 3c-1.9 .4-3.7-.4-3.9-1.7zm-9.1 3.2c-2.2 .2-3.7-.9-3.7-2.4c0-1.3 1.5-2.4 3.5-2.4c1.9-.2 3.7 .9 3.7 2.4c0 1.3-1.5 2.4-3.5 2.4zm-14.3-2.2c-1.9-.4-3.2-1.9-2.8-3.2s2.4-1.9 4.1-1.5c2 .6 3.3 2.1 2.8 3.4c-.4 1.3-2.4 1.9-4.1 1.3zm-12.5-7.3c-1.5-1.3-1.9-3.2-.9-4.1c.9-1.1 2.8-.9 4.3 .6c1.3 1.3 1.8 3.3 .9 4.1c-.9 1.1-2.8 .9-4.3-.6zm-8.5-10c-1.1-1.5-1.1-3.2 0-3.9c1.1-.9 2.8-.2 3.7 1.3c1.1 1.5 1.1 3.3 0 4.1c-.9 .6-2.6 0-3.7-1.5zm-6.3-8.8c-1.1-1.3-1.3-2.8-.4-3.5c.9-.9 2.4-.4 3.5 .6c1.1 1.3 1.3 2.8 .4 3.5c-.9 .9-2.4 .4-3.5-.6zm-6-6.4c-1.3-.6-1.9-1.7-1.5-2.6c.4-.6 1.5-.9 2.8-.4c1.3 .7 1.9 1.8 1.5 2.6c-.4 .9-1.7 1.1-2.8 .4z" />
                                    </svg></a></li>
                        </ul>
                    </div>
                </div>
            </div>

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
