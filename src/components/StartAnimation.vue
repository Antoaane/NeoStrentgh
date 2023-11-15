<script setup>
    import { onMounted } from "vue";
    import NsIcon from "./icons/NsIcon.vue";
    import NsIconGlow from "./icons/NsIconGlow.vue";
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

        gsap.fromTo("#cover1", { y: "0.1%" },
        {
            duration: 1,
            delay: 1.1,
            y: "-100%",
            ease: "expo.inOut",
        }).play();

        gsap.fromTo("#cover2", { y: "-0.1%" },
        {
            duration: 1,
            delay: 1.1,
            y: "100%",
            ease: "expo.inOut",
        }).play();

        gsap.fromTo("#cover1bis", { y: "0.1%" },
        {
            duration: 1,
            delay: 1,
            y: "-100%",
            ease: "expo.inOut",
        }).play();

        gsap.fromTo("#cover2bis", { y: "-0.1%" },
        {
            duration: 1,
            delay: 1,
            y: "100%",
            ease: "expo.inOut",
        }).play();
    });

</script>

<template>
    <div class="start-animation-container">
        <div id="cover1"></div>
        <div id="cover2"></div>
    </div>
    <div class="start-animation-container">
        <div id="cover1bis"></div>
        <div id="cover2bis"></div>
        <NsIcon class="ns-icon" />
    </div>
    
</template>