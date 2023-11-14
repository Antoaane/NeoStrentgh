<script setup>
    import { onMounted } from "vue";
    import NsIcon from "./icons/NsIcon.vue";
    import { gsap } from "gsap";

    onMounted(() => {
        let cover1 = document.getElementById("cover1");
        let cover2 = document.getElementById("cover2");

        gsap.to(".ns-icon", {
            duration: 1,
            delay: 0.2,
            opacity: 0,
            ease: "expo.inOut",
        }).play();

        gsap.to( cover1, {
            duration: 1,
            delay: 1,
            y: "-100%",
            ease: "expo.inOut",
        }).play();;

        gsap.to( cover2, {
            duration: 1,
            delay: 1,
            y: "100%",
            ease: "expo.inOut",
        }).play();;
    });

</script>

<template>
    <div class="start-animation-container">
        <div id="cover1"></div>
        <div id="cover2"></div>
        <NsIcon class="ns-icon" />
    </div>
    
</template>