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
    </div>

    <!-- <div>
        <form @submit.prevent="handleSubmit">
            <div>
                <label for="name">Name:</label>
                <input type="text" id="name" v-model="form.name" />
                <span v-if="errors.name">{{ errors.name }}</span>
            </div>
            <div>
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="form.email" />
                <span v-if="errors.email">{{ errors.email }}</span>
            </div>
            <div>
                <label for="message">Message:</label>
                <textarea id="message" v-model="form.message"></textarea>
                <span v-if="errors.message">{{ errors.message }}</span>

            </div>
            <button type="submit">Submit</button>
        </form>
    </div> -->
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
