<template>
    <div>
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
    </div>
</template>

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

<style></style>