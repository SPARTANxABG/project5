<script setup>
import { faker } from '@faker-js/faker'
const foodname = faker.food.dish()
</script>

<template>
    {{ foodname }} <br />

</template>