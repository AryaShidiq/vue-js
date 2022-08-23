<script setup>
import IconInstagram from './icons/IconInstagram.vue';
import IconFacebook from './icons/IconFacebook.vue';
import IconGithub from './icons/IconGithub.vue';

</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-md d-flex justify-content-evenly align-items-center icon">
                <a href="https://www.instagram.com/arya_shidiq21/" target="_blank"><i class="pt-1">
                    <IconInstagram/>
                </i></a>
                <a href="https://web.facebook.com/arya.shidiq.121" target="_blank"><i class="pt-4">
                    <IconFacebook/>
                </i></a>
                <a href="https://github.com/AryaShidiq?tab=repositories" target="_blank"><i class="pt-4">
                    <IconGithub/>
                </i></a>
            </div>
        </div>
    </div>
</template>

<style scoped>
.icon{
    /* border: 2px solid red; */
    gap: 2.2rem;
}
i{
    font-size: 5rem;
}
</style>