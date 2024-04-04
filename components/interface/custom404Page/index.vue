<template>
    <div class="page__container bg-grey-400">
        <!-- ** class top content -->
        <div class="top-content">
            <h4>ops you got 404 page</h4>
        </div>
        <!-- ** class image wrapper -->
        <div>
            <ClientOnly>
                <Vue3Lottie class="image-wrapper" :animation-data="image" />
            </ClientOnly>
        </div>
        <!-- !! content wrapper -->
        <div class="content-wrapper">
            <!-- *content -->
            <p class="content">we didn't found your page</p>
            <!-- *linkable -->
            <nuxt-link class="linkable" to="/">go home</nuxt-link>
        </div>
    </div>
</template>

<script setup lang="ts">
import { Vue3Lottie } from 'vue3-lottie';
import image from '../../../assets/images/custom/Animation - 1712167010834.json';
</script>

<style lang="css" scoped>
.bg-grey-400 {
    background-color: #606066;
    color: #fff !important;

    
    a {
        color: #fff !important;
    }

    text-transform: capitalize;
}

.top-content {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2.5rem;
}

.image-wrapper {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    width: 15rem;
    height: 15rem;
}

.content-wrapper {
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    width: 700px;
    text-overflow: ellipsis;
    overflow: hidden;
}

.content {
    font-size: 2.5rem;
    font-weight: bold;
}

.linkable {
    text-decoration: none;
    color: black;
    font-size: 1.5rem;
    font-weight: bold;
    animation: updown 1s ease-in-out infinite;
    margin: 1rem 0;
}

@keyframes updown {
    0% {
        transform: translateY(0px);
    }

    50% {
        transform: translateY(10px);
    }

    100% {
        transform: translateY(0px);
    }
}
</style>