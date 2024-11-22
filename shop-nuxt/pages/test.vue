<template>
    <BaseButton outline size="lg" w-full @click="isOpenModal = true"> open / close Modal</BaseButton>
    <BaseModal v-model="isOpenModal">
        <h1>sds</h1>
        <template #footer>
            <BaseButton outline> register</BaseButton>
        </template>
    </BaseModal>
</template>
<script setup lang="ts">
    const isOpenModal = ref(false);
</script>