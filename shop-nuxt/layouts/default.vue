<template>
        <div class="page-wrapper">
            <!-- <Head>
                <Link/>
            </Head> -->
        <!-- start of page-header -->
        <TheHeader></TheHeader>
        <!-- end of page-header -->
        <TheResponsiveHeader></TheResponsiveHeader>
        <!-- start of page-content -->
        <main class="page-content">
            <div class="container">
               <slot/>
            </div>            
        </main>
        <!-- end of page-content -->
        <TheFooter></TheFooter>
    </div>


</template>
<script setup lang="ts">
import TheFooter from '~/components/TheFooter.vue';
import TheHeader from '~/components/TheHeader.vue';
import TheResponsiveHeader from '~/components/TheResponsiveHeader.vue';

useHead({
    link:[
        { rel:"stylesheet" ,href:"/css/dependencies.css"},
        { rel:"stylesheet" ,href:"/css/custom.css.css"},
        { rel:"stylesheet" ,href:"/css/theme.css"},
        { rel:"stylesheet" ,href:"/css/animate.min.css"},
    ],
    script:[
        {src:"/js/dependencies/bootstrap-slider.min.js",body:true},
        {src:"/js/dependencies/bootstrap.bundle.min.js",body:true},
        {src:"/js/dependencies/fancybox.umd.js",body:true},
        {src:"/js/dependencies/iziToast.min.js",body:true},
        {src:"/js/dependencies/jquery-3.6.0.min.js",body:true},
        {src:"/js/dependencies/jquery.countdown.min.js",body:true},
        {src:"/js/dependencies/jquery.simple.timer.min.js",body:true},
        {src:"/js/dependencies/nouislider.min.js",body:true},

        {src:"/js/dependencies/select2.min.js",body:true},
        {src:"/js/dependencies/simplebar.min.js",body:true},
        {src:"/js/dependencies/swiper-bundle.min.js",body:true},
        {src:"/js/dependencies/wNumb.js",body:true},
        {src:"/js/dependencies/zoomsl.min.js",body:true},
        {src:"/js/custom.js",body:true},
        {src:"/js/theme.js",body:true},
    ]
        
})

</script>