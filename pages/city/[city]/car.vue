<script setup>
const route = useRoute();

useHead({
    title: `${route.params.make ? toCapitalize(route.params.make) : 'Cars'} in ${toCapitalize(route.params.city)}`,
});

function toCapitalize(str) {
    return str.charAt(0).toUpperCase() + str.slice(1);
}
</script>

<template>
    <NavBar />
    <!-- begin::Car Section -->
    <section class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-6 sm:px-10 lg:px-16 w-3/5">
        <div class="mt-32 flex">
            <CarSidebar />
            <NuxtPage />
        </div>
    </section>
    <!-- end::Car Section -->
</template>