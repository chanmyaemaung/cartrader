<script setup>
const route = useRoute();

useHead({
    title: toCapitalize(route.params.name)
});

function toCapitalize(str) {
    return str.charAt(0).toUpperCase() + str.slice(1);
}
</script>

<template>
    <NavBar />

    <!-- begin::Card Detail Section -->
    <section class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5">
        <CarDetailHero />
        <CarDetailAttribute />
        <CarDetailDescription />
        <CarDetailContact />
    </section>
    <!-- end::Card Detail Section   -->
</template>